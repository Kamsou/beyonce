<template>
  <div ref="parallaxContainer" :class="containerClasses">
    <div
      class="parallax-background absolute w-full will-change-transform bg-cover bg-no-repeat bg-center"
      :style="backgroundStyle"
    />
  </div>
</template>

<script setup>
const props = defineProps({
  imageUrl: String,
  parallaxRate: {
    type: Number,
    default: 0.5,
  },
  height: {
    type: String,
    default: "300px",
  },
});

const offsetY = ref(0);
const parallaxContainer = ref(null);

const backgroundStyle = computed(() => ({
  backgroundImage: `url(${props.imageUrl})`,
  transform: `translateY(${offsetY.value}px)`,
  inset: "-70px 0px",
}));

const containerClasses = computed(() => `relative overflow-hidden`);

const updateParallax = () => {
  const scrollPosition = window.scrollY;
  const containerTop = parallaxContainer.value?.offsetTop || 0;
  offsetY.value = (scrollPosition - containerTop) * props.parallaxRate;
};

let observer;
const handleIntersection = ([entry]) => {
  if (entry.isIntersecting) {
    window.addEventListener("scroll", updateParallax);
  } else {
    window.removeEventListener("scroll", updateParallax);
  }
};

onMounted(() => {
  if (parallaxContainer.value) {
    observer = new IntersectionObserver(handleIntersection, {
      threshold: 0.1,
    });
    observer.observe(parallaxContainer.value);
  }
});

onBeforeUnmount(() => {
  if (parallaxContainer.value && observer) {
    observer.unobserve(parallaxContainer.value);
  }
  window.removeEventListener("scroll", updateParallax);
});
</script>
