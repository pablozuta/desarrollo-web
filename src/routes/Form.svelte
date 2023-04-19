<script>
  import lamp from './assets/lamp.png';
  import '../app.css';

  import { createClient } from '@supabase/supabase-js';
  import * as yup from 'yup';

  const supabaseUrl = import.meta.env.VITE_SUPABASE_URL;
  const supabaseKey = import.meta.env.VITE_SUPABASE_KEY;
  const supabase = createClient(supabaseUrl, supabaseKey);

  const validationSchema = yup.object({
    nombre: yup.string().required(),
    email: yup.string().email().required(),
    mensaje: yup.string().required(),
  });

  let nombre = '';
  let email = '';
  let mensaje = '';

  async function submitForm() {
    const { error } = await supabase
      .from('contacto')
      .insert({ nombre, email, mensaje });

    if (error) {
      console.error(error);
    } else {
      nombre = '';
      email = '';
      mensaje = '';
    }
    alert('✔️✔️Mensaje enviado exitosamente.');
  }

  function handleSubmit(event) {
    event.preventDefault();

    validationSchema
      .validate({ nombre, email, mensaje })
      .then(() => {
        submitForm();
      })
      .catch((error) => {
        console.error(error);
      });
  }
</script>

<section
  aria-labelledby="contact"
  class="container mx-auto px-8 overflow-hidden"
>
  <div class="flex flex-wrap justify-center gap-12 md:gap-6 lg:gap-20">
    <div class="md:flex-1 md:max-w-sm relative">
      <img src={lamp} alt="Lamp" class="mx-auto mt-20" />

      <div
        class="
            absolute
            -bottom-18
            left-1/2
            -translate-x-1/2
            -z-10
            aspect-square
            md:border-8
            border-amber-400
            rounded-full
            md:w-72
            lg:w-96
          "
      />
    </div>

    <!-- FORM -->
    <form
      on:submit={handleSubmit}
      class="
          relative
          border-8
          border-neutral-900
          p-6
          rounded-lg
          grid
          gap-8
          md:flex-1
          md:max-w-lg
          my-4
          md:my-12
          lg:my-16
          bg-white
          dark:bg-neutral-800
          w-full
      "
    >
      <h2 id="contact" class="text-3xl font-bold">Contactanos</h2>
      <div class="relative">
        <input
          type="text"
          id="nombre"
          name="nombre"
          bind:value={nombre}
          class="
          peer
          form-input
          w-full
          border-4
          border-amber-400
          rounded-md
          focus:ring-4
          dark:focus:ring-offset-2
          focus:ring-amber-400
          focus:border-amber-400
          focus:outline-none
          dark:bg-amber-400
          dark:text-neutral-900
          placeholder-transparent
      "
          placeholder="Your Name"
        />
        <label
          for="name"
          class="
        text-neutral-500
        text-sm
        font-bold
        uppercase
        absolute
        -top-4
        left-2
        -translate-y-1/2
        transition-all
        peer-placeholder-shown:left-4
        peer-placeholder-shown:top-1/2
        peer-placeholder-shown:text-neutral-900
        peer-focus:-top-4
        peer-focus:left-2
        peer-focus:text-neutral-600
        dark:peer-focus:text-neutral-300
      "
        >
          Nombre
        </label>
      </div>
      <div class="relative">
        <input
          type="email"
          id="email"
          name="email"
          bind:value={email}
          class="
          peer
          form-input
          w-full
          border-4
          border-amber-400
          rounded-md
          focus:ring-4
          dark:focus:ring-offset-2
          focus:ring-amber-400
          focus:border-amber-400
          focus:outline-none
          dark:bg-amber-400
          dark:text-neutral-900
          placeholder-transparent
        "
          placeholder="Your Email"
        />
        <label
          for="email"
          class="
        text-neutral-500
        text-sm
        font-bold
        uppercase
        absolute
        -top-4
        left-2
        -translate-y-1/2
        transition-all
        peer-placeholder-shown:left-4
        peer-placeholder-shown:top-1/2
        peer-placeholder-shown:text-neutral-900
        peer-focus:-top-4
        peer-focus:left-2
        peer-focus:text-neutral-600
        dark:peer-focus:text-neutral-300
      "
        >
          Email
        </label>
      </div>
      <div class="relative">
        <textarea
          id="mensaje"
          name="mensaje"
          bind:value={mensaje}
          cols="20"
          rows="5"
          class="
        peer
        form-textarea
        resize-none
        w-full
        border-4
        border-amber-400
        rounded-md
        focus:ring-4
        dark:focus:ring-offset-2
        focus:ring-amber-400
        focus:border-amber-400
        focus:outline-none
        dark:bg-amber-400
        dark:text-neutral-900
        placeholder-transparent
      "
          placeholder="How can we help?"
        />
        <label
          for="content"
          class="
          text-neutral-500
          text-sm
          font-bold
          uppercase
          absolute
          -top-3
          left-2
          -translate-y-1/2
          transition-all
          peer-placeholder-shown:left-4
          peer-placeholder-shown:top-6
          peer-placeholder-shown:text-neutral-900
          peer-focus:-top-4
          peer-focus:left-2
          peer-focus:text-neutral-600
          dark:peer-focus:text-neutral-300
        "
        >
          Como Podemos Ayudarte?
        </label>
      </div>
      <button
        type="submit"
        class="
      py-2
      px-6
      bg-neutral-900
      text-white
      w-max
      shadow-xl
      hover:shadow-none
      transition-shadow
      focus:outline-none
      focus-visible:ring-4
      ring-neutral-900
      rounded-md
      ring-offset-4
      ring-offset-white
      dark:ring-offset-amber-400
    "
      >
        Enviar
      </button>
    </form>
  </div>
</section>
