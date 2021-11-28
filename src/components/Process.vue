<template>
  <div class="process_management">
    <p class="section_title">{{ sectionTitle }}</p>
    <h2>
      <span class="title_bg">{{ title.marked }}</span> {{ title.notMarked }}
    </h2>
    <p class="info_text">
      {{ description }}
    </p>

    <div class="process">
      <div class="process_list d_flex">
        <div v-for="process in processManagement" :key="process.processId">
          <p class="number">{{ process.processId }}</p>
          <h4>{{ process.processName }}</h4>
          <p>{{ process.processDesc }}</p>
        </div>
      </div>
    </div>
    <!-- /.process -->
  </div>
  <!-- /.process_management -->
</template>

<script>
export default {
  data() {
    return {
      sectionTitle: "How it works in practice",
      title: {
        marked: "Process",
        notMarked: "Management",
      },
      description: `We work with innovative methodologies to ensure that the entire
      reformatting process is done from start to finish as planned.`,
      processManagement: [
        {
          processId: "01",
          processName: "Collection of information",
          processDesc: "Lorem ipsum dolor sit amet consectetur.",
        },
        {
          processId: "02",
          processName: "Strategic planning",
          processDesc: "Lorem ipsum dolor sit amet consectetur.",
        },
        {
          processId: "03",
          processName: "Assignment of responsabilities",
          processDesc: "Lorem ipsum dolor sit amet consectetur.",
        },
        {
          processId: "04",
          processName: "Formatting process",
          processDesc: "Lorem ipsum dolor sit amet consectetur.",
        },
        {
          processId: "05",
          processName: "Continuity formalization",
          processDesc: "Lorem ipsum dolor sit amet consectetur.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.process_management {
  padding: 130px 0;
  color: $nexgen_grey;
  font-weight: 300;
  text-align: center;

  h2 {
    color: $nexgen_secondary_color;

    .title_bg {
      background-color: rgba($nexgen_primary_color, 0.15);
      color: $nexgen_primary_color;
    }
  }

  .info_text {
    width: 40%;
    margin: auto;
  }

  .process {
    margin-top: 5rem;
    border-top: 5px solid rgba($nexgen_primary_color, 0.15);

    .process_list {
      width: 80%;
      margin: auto;
      margin-top: -1.6rem;
      align-items: flex-start;
      gap: 2rem;

      .number {
        display: flex;
        justify-content: center;
        align-items: center;
        margin: auto;
        width: 45px;
        height: 45px;
        background-color: #daeced;
        border-radius: 50%;
        font-size: 1.2rem;
        font-weight: 700;
        color: $nexgen_primary_color;
      }

      h4 {
        color: $nexgen_secondary_color;
        margin: 1rem 0;
        line-height: 1.8rem;
      }

      & > div:hover {
        cursor: crosshair;

        .number {
          background-color: $nexgen_primary_color;
          color: $nexgen_white;
        }
      }
    }
  }
}
</style>