<template>
  <div class="top-content">
    <h1 v-text="title" />
    <base-button
      :to="{ name: 'dataset-id-annotation-mode', params: { id: datasetId } }"
      class="secondary text"
    >
      <svgicon name="chevron-left" width="10" height="10" color="#4C4EA3" />
      {{ goToDatasetPageLabel }}
    </base-button>
  </div>
</template>

<script>
export default {
  name: "TopDatasetSettingsFeedbackTaskContent",
  props: {
    datasetId: {
      type: String,
      required: true,
    },
  },
  created() {
    this.title = "Dataset settings";
    this.goToDatasetPageLabel = "See your dataset";
  },
};
</script>

<style lang="scss" scoped>
.top-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100%;
  border-bottom: 1px solid #e6e6e6;
}
</style>
