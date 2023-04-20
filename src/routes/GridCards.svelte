<script>
  import dots from './assets/dots.svg';
  import '../app.css';
</script>

<section aria-labelledby="qualities" class="relative">
  <img
    src={dots}
    class="
  hidden
  lg:block
  absolute
  top-1/2
  -translate-y-1/2
  -left-24
  xl:-left-7
  "
    alt="dots"
    aria-hidden="true"
  />
  <img
    src={dots}
    class="
  hidden
  lg:block
  absolute
  top-1/2
  -translate-y-1/2
  -right-24
  xl:-right-7
  "
    alt="dots"
    aria-hidden="true"
  />
  <h2 id="qualities" class="sr-only">Our Qualities</h2>
  <div
    class="container
    mx-auto
    max-w-5xl
    flex
    gap-12
    flex-wrap
    items-start
    justify-center
    md:justify-between
  "
  >
    <div
      class="
    grid
    gap-4
    justify-items-center
    text-center
    md:flex-1
  "
    >
      <div class="rounded-full border-8 border-amber-600 p-3">
        <img
          class="h-14 w-14"
          src="https://www.svgrepo.com/show/241677/sms.svg"
          alt="design icon"
        />
      </div>
      <h3 class="text-3xl font-bold">Diseño</h3>
      <p>
        Cada detalle cuenta. Por eso, nuestra pasión por el diseño se refleja en
        cada proyecto que emprendemos.
      </p>
    </div>
    <div
      class="
    grid
    gap-4
    justify-items-center
    text-center
    md:flex-1
    "
    >
    <div class="rounded-full border-8 border-amber-600 p-3">
        <img
          class="h-14 w-14"
          src="https://www.svgrepo.com/show/241668/hierarchical-structure-hierarchy.svg"
          alt="technology icon"
        />
      </div>
      <h3 class="text-3xl font-bold">Tecnología</h3>
      <p>
        Nuestra obsesion con la tecnología nos lleva a buscar siempre las
        mejores soluciones para nuestros clientes.
      </p>
    </div>
    <div
      class="
    grid
    gap-4
    justify-items-center
    text-center
    md:flex-1
    "
    >
      <div
        class="
      rounded-full
      border-8
      border-amber-600
      p-3
      "
      >
        <img
          class="h-14 w-14"
          src="https://www.svgrepo.com/show/241659/24-hours-help.svg"
          alt="efficiency icon"
        />
      </div>
      <h3 class="text-3xl font-bold">Eficiencia.</h3>
      <p>
        Creemos que la eficiencia es fundamental. Por eso, optimizamos nuestros
        procesos para ofrecer el mejor servicio posible.
      </p>
    </div>
  </div>
</section>
