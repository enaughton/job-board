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
  <div>
    <div class="max-w-4xl mx-auto sm:px-6 lg:px-8">
      <div
        v-for="job in jobs"
        :key="job.title"
        class="p-6 mt-8 overflow-hidden bg-white shadow sm:rounded-lg"
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
  </div>
</template>
