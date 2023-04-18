<script>
  import '../app.css';
  import secondaryImage from './assets/table.png';
  import Form from './Form.svelte';
  import GridCards from './GridCards.svelte';
  import Partners from './Partners.svelte';
</script>

<main class="max-w-[2000px] mx-auto text-neutral-900 dark:text-neutral-200 bg-white dark:bg-neutral-800">

  <main class="grid gap-12 sm:gap-16 md:gap-24 lg:gap-32 px-8
  overflow-hidden " >
  
    <section aria-labelledby="home" class="relative mt-10">
      <div class="flex flex-wrap-reverse gap-8 justify-center">
        <div
          class="flex gap-6 flex-wrap flex-col items-start lg:justify-center"
        >
          <div class="flex flex-wrap flex-col items-start gap-2">
            <h2 class="text-5xl font-bold text-orange-300">
              Un servicio Innovador.
            </h2>
            <p class="max-w-md text-xl">
              Nuestro enfoque es siempre el futuro. Por eso, estamos
              constantemente buscando nuevas soluciones e ideas innovadoras.
            </p>
          </div>
          <br />
        </div>
        <img src={secondaryImage} alt="Table" />
      </div>

      <div
        class="
    bg-amber-400
    h-24
    xl:h-48
    -mx-8
    mt-12
    xl:mt-0
    xl:absolute
    w-screen
    -bottom-8
    -z-10
"
      />
    </section>

    <GridCards />

    <Partners />
  </main>

  <Form />
</main>

<style lang="postcss">
  @import url('https://fonts.googleapis.com/css2?family=Merriweather:wght@700&display=swap');
</style>
