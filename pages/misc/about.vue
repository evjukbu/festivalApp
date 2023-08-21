<template>
  <CardLikeContainer>
    <h1 class="text-3xl pb-3">Über diese App</h1>
  </CardLikeContainer>
  <div class="flex flex-col space-y-3">
    <div class="card card-compact w-full bg-base-100 shadow-xl">
      <div class="card-body">
        <h2 class="card-title">Jugendfestival App Version {{ version }}</h2>
        <figure class="flex justify-center">
          <img src="/icon.png" class="w-1/2" />
        </figure>
        <span class="text-center">Copyright © 2023 Evangelische Jugend im Kirchenkreis Burgdorf.</span>
      </div>
    </div>
    <div class="card card-compact w-full bg-base-100 shadow-xl">
      <div class="card-body">
        <h2 class="card-title">Autor</h2>
        <div class="flex justify-center">
          <div class="avatar placeholder">
            <div class="bg-success text-base-100 rounded-full w-16">
              <span class="text-2xl">JK</span>
            </div>
          </div>
        </div>
        <span class="text-center">Jens Krieger-Juhnke</span>
        <div class="flex justify-center flex-row">
          <a href="mailto:jens@evju-uetze.de">
            <button class="btn btn-xl btn-ghost">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round"
                  d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75" />
              </svg>

            </button>

          </a>
          <a href="https://instagram.com/__sensens_">
            <button class="btn btn-xl btn-ghost">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round"
                  d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12z" />
              </svg>

            </button>


          </a>
        </div>
      </div>
    </div>
    <div class="card card-compact w-full bg-base-100 shadow-xl">
      <div class="card-body">
        <h2 class="card-title">Changelog</h2>
        <div v-for="entry in changelog">
          <span><b>{{ entry.date }}</b></span>
          <ul class="list-disc list-inside">
            <li v-for="change in entry.changes">{{ change }}</li>
          </ul>
        </div>
      </div>
    </div>
    <br />
  </div>
</template>

<script setup>
const version = "1.0"

const changelog = [
  {
    date: "16. August 2023",
    changes: [
      "change: Das Festival Logo wird nun unter 'Über diese App' verwendet.",
      "change: Die aktuelle Version des Festival Logos wird verwendet."
    ]
  },
  {
    date: "13. August 2023",
    changes: [
      "Change: Allgemeine Layout Verbesserungen bei Spacing"
    ]
  },
  {
    date: "12. August 2023",
    changes: [
      "Added: Logo in der About Page",
      "Change: Passende Werte im Manifest der PWA",
      "Change: Verbessertes Spacing im 'Über diese App' Bildschirm"
    ]
  },
  {
    date: "11. August 2023",
    changes: [
      "Added: Neue Seite 'Über diese App'",
      "Fix: Das ausgewählte Design wird für die ganze Seite verwendet",
      "Fix: Seiten mit viel Text werden nicht mehr abgeschnitten"
    ]
  },
  {
    date: "08. August 2023",
    changes: [
      "Added: Mehrere Farbthemen",
      "Added: Neue Seite 'Designs'",
      "Changed: Seiten haben jetzt Titel"
    ]
  },
  {
    date: "07. August 2023",
    changes: [
      "Added: Die App erfüllt nun die Anforderungen einer TWA",
      "Changed: Layoutverbesserungen in der Veranstaltungsliste",
      "Changed: Allgemeines Refactoring"
    ]
  }
]
</script>