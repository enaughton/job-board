<script>
export default {
  name: "IndexPage",
};
</script>


<template>
  <div class="bg-gradient-to-br from-green-600">
    <link
      href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css"
      rel="stylesheet"
    />

    <Header />
    <Board>
      <JobPost />
    </Board>
  </div>
</template>

