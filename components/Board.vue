<script>
data: {
  jobs: [
    {
      title: "Save Hyrule",
      description:
        "Looking for somebody to come save the day! Please there are monsters all over place",
      benefits: ["Unlimited breakable pots", "Gems", "other sidequests"],
    },
    {
      title: "Mushroom Kingdom is under again",
      description:
        "2. Show checkboxes in a vertical list/column instead of a row",
      checked: false,
    },
  ];
}
</script>




<template>
  <div>
    <div
      v-for="job in jobs"
      :key="job.title"
      class="relative min-h-screen bg-gray-100  items-top sm:items-center sm:pt-0"
    >
      <JobPost />
    </div>
  </div>
</template>
