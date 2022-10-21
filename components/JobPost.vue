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
      class="p-4 mt-8 sm:rounded-lg bg-gradient-to-tr from-green-600"
    >
      <h2 class="text-2xl font-semibold leading-7">{{ job.title }}</h2>
      <p class="mt-4 text-gray-600">{{ job.description }}</p>
      <ul class="p-4">
        <li v-for="item in job.benefits" :key="item" class="list-disc">
          {{ item }}
        </li>
      </ul>
    </div>
  </div>
</template>
