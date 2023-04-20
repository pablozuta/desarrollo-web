<script>
  import '../app.css';
  import Form from './Form.svelte';
  import GridCards from './GridCards.svelte';
  import Hero from './Hero.svelte';
  import Partners from './Partners.svelte';
</script>

<main
  class="max-w-[2000px] mx-auto text-neutral-900 dark:text-neutral-200 bg-white dark:bg-neutral-800"
>
  <main
    class="grid gap-12 sm:gap-16 md:gap-24 lg:gap-32 px-8
  overflow-hidden"
  >
    <Hero />

    <GridCards />

    <Partners />
  </main>

  <Form />
</main>

<style lang="postcss">
  @import url('https://fonts.googleapis.com/css2?family=Merriweather:wght@700&display=swap');
</style>
