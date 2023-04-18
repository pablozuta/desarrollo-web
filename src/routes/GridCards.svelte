<script>
  import dots from './assets/dots.svg'
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
        <div
          class="
        rounded-full
        border-8
        border-amber-400
        p-4
      "
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-14 w-14"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"
            />
          </svg>
        </div>
        <h3 class="text-3xl font-bold">Diseño</h3>
        <p>
          Cada detalle cuenta. Por eso, nuestra pasión por el diseño se
          refleja en cada proyecto que emprendemos.
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
      border-amber-400
      p-4
      "
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-14 w-14"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M13 10V3L4 14h7v7l9-11h-7z"
            />
          </svg>
        </div>
        <h3 class="text-3xl font-bold">Tecnología</h3>
        <p>
          Nuestra pasión por la tecnología nos lleva a buscar siempre las
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
      border-amber-400
      p-4
      "
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-14 w-14"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z"
            />
          </svg>
        </div>
        <h3 class="text-3xl font-bold">Eficiencia.</h3>
        <p>
          Creemos que la eficiencia es fundamental en todo lo que hacemos. Por
          eso, optimizamos nuestros procesos y tecnologías para ofrecer el
          mejor servicio posible.
        </p>
      </div>
    </div>
  </section>