<script>
import jobs from "/jobs.json";
export default {
  data() {
    return {
      jobs: jobs,
    };
  },
};
</script>

  <template>
  <div class="pt-4 pb-8">
    <div
      v-for="job in jobs"
      :key="job.title"
      class="p-4 mt-8  sm:rounded-lg bg-gradient-to-tr from-green-600 hover:bg-white"
    >
      <div class="flex flex-row content-around gap-8">
        <h2 class="text-2xl font-semibold leading-7">{{ job.title }}</h2>
      </div>
      <p class="mt-4">{{ job.description }}</p>
      <ul class="p-4">
        <li v-for="item in job.benefits" :key="item" class="list-disc">
          {{ item }}
        </li>
      </ul>

      <a
        class="p-2 overflow-hidden text-white bg-blue-500 rounded"
        :href="'mailto:' + job.email + '?subject=' + job.title"
      >
        Email Us
      </a>
    </div>
  </div>
</template>
