<script>
  let showContacts = false;

  function toggleContacts() {
    showContacts = !showContacts;
  }


  let count = 0;

  $: if (count >= 5) {
		alert("I think I know this resume by now, let's offer Walid a job :)");
		count = 0;
	}

  function increment() {
    count += 1;
}
</script>


<style>
  .toggle-btn {
    cursor: pointer;
    padding: 10px;
    background-color: #3490dc;
    color: #fff;
    border: blue;
    border-radius: 5px;
  }
</style>



<div class="container mx-auto border">
  <div class="grid grid-cols-12">
    <!-- Left column -->
    <div id="leftColumn" class="col-span-12 md:col-span-6 lg:col-span-4">
      <!-- Profile Picture -->
      <div id="profilePicture">
        <img
          src="src/lib/photo_cv_bonne_qualité.JPG"
          alt="My profile picture"
          class="w-1/2 mx-auto rounded-full"
        />
      </div>

      <!-- Contacts -->
      <div id="blockContact" class="px-4 lg:px-16 mt-3">
        <div class="text-xl font-bold uppercase">CONTACT</div>
        <button class=toggle-btn on:click={toggleContacts}>Toggle Contacts</button>

        {#if showContacts}
          <div>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-5 h-5 inline"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 0 0 2.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 0 1-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 0 0-1.091-.852H4.5A2.25 2.25 0 0 0 2.25 4.5v2.25Z"
              />
            </svg>
            <span class="ml-2">+33 7 67 76 29 01</span>
          </div>
          <div>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-5 h-5 inline"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75"
              />
            </svg>
            <span class="ml-2">walid.essabar@essec.edu</span>
          </div>
          <div>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-5 h-5 inline"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M15 10.5a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z"
              />
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1 1 15 0Z"
              />
            </svg>
            <span class="ml-2">Paris, France</span>
          </div>
        {/if}
      </div>

      <div id="blockProfile" class="px-4 lg:px-16 mt-3">
        <div class="text-xl font-bold uppercase">Profile</div>
        <div>
          Video games have always made me dream, so I believe it is now my turn
          to make other players dream. I am looking to build a path from the
          passion that drives me, by making video games a part of my life both
          professionally and on a more personal level, through associative work.
        </div>
      </div>

      <!-- Languages -->
      <div id="blockLanguage" class="px-4 lg:px-16 mt-3">
        <div class="text-xl font-bold uppercase">Languages</div>
        <div class="grid grid-cols-12">
          <div class="col-span-12 lg:col-span-4">French</div>
          <div class=" col-span-12 lg:col-span-8 my-auto">
            <div
              class="h-4 bg-sky-200 rounded-full dark:bg-blue-500 my-auto"
              style="width: 100%"
            ></div>
          </div>
          <div class="col-span-12 lg:col-span-4">English</div>
          <div class=" col-span-12 lg:col-span-8 my-auto">
            <div
              class="h-4 bg-sky-200 rounded-full dark:bg-blue-500 my-auto"
              style="width: 90%"
            ></div>
          </div>
        </div>
      </div>

      <!-- Skills -->
      <div id="blockSkills" class="px-4 lg:px-16 mt-3">
        <div class="text-xl font-bold uppercase">Skills</div>
        <ul class="list-disc ml-5">
          <li>Office Suite</li>
          <li>Jira, Confluence</li>
          <li>Trello</li>
        </ul>
      </div>


      <!-- Read button -->
      <div id="blockSkills" class="px-4 lg:px-16 mt-3">
        <div class="text-xl font-bold uppercase">CV READINGS</div>
        <button class=toggle-btn on:click={increment}>
            I have read this CV {count}
            {count <= 1 ? "time. I could do more ..." : "times! That's awesome!"}
          </button>
        </div>
    </div>





    <!-- Right column -->
    <div
      id="rightColumn"
      class="col-span-12 md:col-span-6 lg:col-span-8 bg-sky-200 p-5"
    >
      <!-- Name & Title -->
      <div id="blockName">
        <div class="text-6xl font-bold">Walid ESSABAR</div>
        <div class="text-4xl uppercase mt-2">Video game Associate Producer</div>
      </div>

      <!-- Work experience -->
      <div id="blockWork" class="mt-4">
        <div class="uppercase font-bold text-3xl bg-white p-2">
          Work Experience
        </div>

        <!-- Work experience 1 -->
        <div id="work1" class="p-2">
          <div class="text-2xl font-bold">Ubisoft Paris Studio</div>
          <div class="text-lg text-gray-500">
            Project Assistant – Just Dance Next
          </div>
          <ul class="list-disc p-4">
            <li>
              Followed 2 features of the game in SCRUM framework: handled
              meetings, organized the work, oversaw the tasks’ progress in JIRA
            </li>
            <li>
              Assisted the project’s top management team: organized and
              participated in weekly/yearly meetings, created post-mortems, …
            </li>
            <li>
              Took part in the agile committee responsible for improving the
              production organization: surveys, agile rituals, documentation
            </li>
          </ul>
        </div>

        <!-- Work experience 2 -->
        <div id="work2" class="p-2">
          <div class="text-2xl font-bold">Ubisoft Paris Studio</div>
          <div class="text-lg text-gray-500">
            Product Manager Assistant – AAA Project
          </div>
          <ul class="list-disc p-4">
            <li>
              Redesign of the brand identity through a competitive benchmark on
              the shooter market (communication, USP, live strategy)
            </li>
            <li>
              Developped Player Cards based on the analysis of the brand
              audience and synthesizing the knowledge of production teams
            </li>
            <li>
              Used agile project management tools (JIRA, Confluence) to
              facilitate access to information and help cooperation between
              teams
            </li>
          </ul>
        </div>

        <!-- Studies -->
        <div id="blockEducation" class="mt-4">
          <div class="uppercase font-bold text-3xl bg-white p-2">Education</div>
        </div>

        <!-- Studies 1 -->
        <div id="studies1" class="p-2">
          <div class="text-2xl font-bold">Master in Management</div>
          <div class="text-lg">
            ESSEC Business School <span class="text-gray-500">2020 - 2024</span>
          </div>
        </div>

        <!-- Studies 2 -->
        <div id="studies2" class="p-2">
          <div class="text-2xl font-bold">
            Preparatory classes for Business Schools
          </div>
          <div class="text-lg">
            Lycée Chateaubriand <span class="text-gray-500">2018 - 2020</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
