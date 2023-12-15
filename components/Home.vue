<script setup>
useHead({
  title: "Beyoncé — Renaissance",
  meta: [
    {
      name: "description",
      content:
        "Plongez dans l'univers de 'Renaissance' - le dernier chef-d'œuvre musical de Beyoncé. Explorez chaque piste, découvrez les inspirations derrière l'album, et rejoignez la communauté des fans pour célébrer l'icône de la musique moderne. Découvrez des interviews exclusives, des clips, des photos et rejoignez-nous dans cette expérience musicale inoubliable.",
    },
  ],
});

const { $gsap } = useNuxtApp();

const isSwitchOn = ref(false);

onMounted(() => {
  $gsap.to(".silver", {
    scale: 1.1,
    duration: 2,
    repeat: -1,
    yoyo: true,
    ease: "power1.inOut",
  });
});
</script>

<template>
  <section class="bg-[#090705] text-white font-regular">
    <div
      class="flex justify-between absolute w-full px-4 sm:px-16 pt-9 text-sm sm:text-[1.5vw] text-[#EBFF00] font-title flex-wrap gap-2"
    >
      <h1>Renaissance</h1>
      <h2>Beyonce</h2>
    </div>

    <Switch
      v-model="isSwitchOn"
      class="absolute sm:bottom-16 sm:right-16 bottom-16 right-[50%] transform translate-x-[50%] sm:translate-x-0"
      audioSrc="https://res.cloudinary.com/augalo/video/upload/v1702666945/Beyonc%C3%A9/beyonce-song_jrnjvi.mp3"
    />

    <img
      src="https://res.cloudinary.com/augalo/image/upload/v1702660154/Beyonc%C3%A9/220420_M22_LA_Jacobs_Renaissance_Horse_0075_V14_SF_QC_1-1_2_pmhdg9.webp"
      alt="Beyoncé sur son cheval en argent"
      class="h-screen w-screen object-cover object-top"
    />

    <p
      class="sm:text-[2.500vw] text-[#EBFF00] font-title text-center text-xl px-4 -mt-[30px]"
    >
      N’oubliez jamais de creer
    </p>

    <div class="sm:px-[16.667vw] px-6 pt-[17vw] sm:pt-[12.847vw]">
      <div class="flex flex-col sm:flex-row gap-[8.889vw] items-center">
        <div class="w-full sm:w-[50%]">
          <ParallaxImage
            imageUrl="https://res.cloudinary.com/augalo/image/upload/v1702675003/Beyonc%C3%A9/Beyonce-film-recap_2_poyvnd.webp"
            :parallaxRate="0.1"
            class="h-[50vw] sm:h-[20vw]"
          />
        </div>

        <div class="sm:w-[50%]">
          <p class="sm:text-[1.1vw] text-base">
            Beyoncé Knowles-Carter, mondialement connue sous le nom de Beyoncé,
            est une chanteuse, compositrice, productrice et actrice américaine,
            née le 4 septembre 1981 à Houston, au Texas. Elle est reconnue pour
            sa voix puissante, ses performances dynamiques et son influence
            culturelle significative. Sa carrière a commencé dans les années
            1990 avec le groupe R&B Destiny's Child, l'un des groupes féminins
            les plus vendus de tous les temps. <br /><br />

            Après le succès de Destiny's Child, Beyoncé a lancé sa carrière solo
            en 2003 avec l'album "Dangerously in Love", qui a été un succès
            commercial et critique, incluant des hits comme "Crazy in Love" et
            "Baby Boy". Son talent et sa polyvalence lui ont permis de s'imposer
            rapidement comme une des plus grandes artistes de sa génération.
          </p>
        </div>
      </div>

      <div class="flex justify-center pt-[9vw] py-[20vw]">
        <p class="sm:-[36.389vw] w-full sm:w-[45vw] sm:text-[1.1vw] text-base">
          Au cours de sa carrière, Beyoncé a sorti plusieurs albums acclamés,
          tels que "B'Day", "I Am... Sasha Fierce", "4", "Beyoncé" et
          "Lemonade". Chacun de ces albums a démontré son habileté à mélanger
          différents genres musicaux et à aborder des thèmes comme l'amour,
          l'empowerment des femmes, et les questions raciales et sociales.
        </p>
      </div>

      <div class="relative mt-12 sm:mt-0">
        <img
          src="https://res.cloudinary.com/augalo/image/upload/v1702658427/Beyonc%C3%A9/silverpaper_hq3im9.webp"
          class="silver w-[70%] sm:w-[25vw] absolute top-[50%] left-[50%] transform -translate-x-1/2 -translate-y-1/2"
          alt=""
        />
        <p
          class="relative z-10 sm:text-[2.5vw] text-xl text-[#EBFF00] font-title text-center mb-44 sm:mb-[25vw] bg-black p-3"
        >
          La confiance en soi
        </p>
      </div>

      <div>
        <img
          src="https://res.cloudinary.com/augalo/image/upload/v1702675311/Beyonc%C3%A9/img_yhyp32.webp"
          class="sm:w-[25vw]"
          alt=""
        />

        <div class="pb-[3vw] pt-[8vw]">
          <p class="sm:text-[1.1vw] text-base sm:w-[36.389vw] mx-auto">
            En plus de sa carrière musicale, Beyoncé a également joué dans
            plusieurs films, y compris "Austin Powers in Goldmember",
            "Dreamgirls" et "The Lion King", où elle a prêté sa voix à Nala.
            <br /><br />

            Beyoncé est également connue pour son travail humanitaire et son
            activisme. Elle a contribué à diverses causes, notamment la
            sensibilisation aux droits des femmes, l'éducation et la lutte
            contre la faim.
          </p>
        </div>

        <div class="flex justify-end">
          <img
            src="https://res.cloudinary.com/augalo/image/upload/v1702660486/Beyonc%C3%A9/beyonce-11_vl52ps.png"
            class="sm:w-[25vw]"
            alt=""
          />
        </div>
      </div>

      <p
        class="sm:text-[2.500vw] pb-10 text-[#EBFF00] font-title text-center mt-[12.361vw]"
      >
        Le travail, la discipline
      </p>
    </div>
  </section>

  <footer
    class="bg-[#090705] text-white sm:pt-64 pt-10 pb-14 flex sm:justify-end justify-center px-[16.667vw]"
  >
    <div class="flex flex-col sm:flex-row justify-between sm:w-[205px]">
      <span>Link</span>
      <span>Link</span>
      <span>Link</span>
    </div>
  </footer>
</template>
