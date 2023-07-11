<script lang="ts">
  import Header from "../components/landing-page/Header.svelte";
  import Footer from "../components/landing-page/Footer.svelte";
  import Link from "../components/navigation/Link.svelte";
  import Text from "../components/typography/Text.svelte";
  import LinkButton from "../components/buttons/LinkButton.svelte";

  interface Feature {
    name: string;
    description: string;
  }

  const features: Feature[] = [
    {
      name: "One Page PDF",
      description:
        "one-page PDF for entire webpage",
    },
    {
      name: "Multiple Page PDF",
      description:
        "multiple-page PDF for entire webpage",
    },
    {
      name: "Custom Page Size",
      description:
        "support custom paper size, eg. window size, A4, A3, Letter and so on",
    },
    {
      name: "Scalebale, Printable",
      description:
        "screenshot, but PDF format.",
    },
    {
      name: "Multiple Tabs Batch Export",
      description:
        "export PDF with multiple tabs  at one time",
    },
  ];
</script>

<svelte:head>
  <title>Just One Page PDF</title>
</svelte:head>

<div>
  <Header />
  <main class="flex flex-col justify-center">
    <section
      id="hero-section"
      class="w-full h-full px-6 py-12 flex flex-col justify-start items-center gap-10 relative"
    >
      <div class="w-full max-w-5xl flex flex-col items-center gap-8 pt-20">
        <div
          class="w-full min-w-[320px] max-w-lg flex flex-col items-center gap-8 text-center"
        >
          <div class="flex flex-col gap-4">
            <Text as="h1">Just One Page PDF</Text>
            <Text as="p">
               Save the entire webpage as a one-page PDF.
            </Text>
          </div>
          <LinkButton
            link="https://chrome.google.com/webstore/detail/just-one-page-pdf/fgbhbfdgdlojklkbhdoilkdlomoilbpl?hl=en"
            textLabel="Install for free"
            endIcon="chevron_right"
            variant="primary"
            size="large"
          />
        </div>
        <div
          class="transition w-full min-w-[320px] max-w-xl aspect-video bg-slate-500/20 rounded-2xl overflow-hidden"
          title="Just One Page PDF"
          style="outline: 3px solid;"
        >
        <img src="/hero.png" style="object-fit: none;"/>
        </div>
      </div>
    </section>
    <section
      id="features"
      class="w-full px-6 py-12 flex justify-center items-center"
    >
      <div class="w-full h-full max-w-5xl flex flex-col items-center gap-6">
        <div class="text-center max-w-lg">
          <Text as="h2">A Fine Set Of Features For Your Productivity</Text>
        </div>

        <div
          class="w-full py-6 flex flex-wrap justify-center items-center gap-6"
        >
          {#each features as feature}
            <article
              class="card card-normal min-w-min w-full max-w-sm bg-slate-500/20"
            >
              <div class="card-title pt-4 px-4">
                <Text as="h5">{feature.name}</Text>
              </div>
              <div class="card-body">
                <Text as="p">{feature.description}</Text>
              </div>
            </article>
          {/each}
        </div>
        <LinkButton
          link="https://chrome.google.com/webstore/detail/just-one-page-pdf/fgbhbfdgdlojklkbhdoilkdlomoilbpl?hl=en"
          textLabel="Install for free"
          endIcon="chevron_right"
          variant="primary"
          size="large"
        />
      </div>
    </section>
  </main>
  <Footer />
</div>
