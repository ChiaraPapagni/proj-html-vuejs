<template>
  <div class="management">
    <p class="section_title">How it works in practice</p>
    <h3><span class="title_bg">Process</span> Management</h3>
    <p class="info_text">
      We work with innovative methodologies to ensure that the entire
      reformatting process is done from start to finish as planned.
    </p>

    <div class="process">
      <div class="process_list d_flex">
        <div class="information">
          <p class="number">01</p>
          <h5>Collection of information</h5>
          <p>Lorem ipsum dolor sit amet consectetur.</p>
        </div>
        <div class="planing">
          <p class="number">02</p>
          <h5>Strategic planning</h5>
          <p>Lorem ipsum dolor sit amet consectetur.</p>
        </div>
        <div class="responsibilities">
          <p class="number">03</p>
          <h5>Assignment of responsabilities</h5>
          <p>Lorem ipsum dolor sit amet consectetur.</p>
        </div>
        <div class="formatting">
          <p class="number">04</p>
          <h5>Formatting process</h5>
          <p>Lorem ipsum dolor sit amet consectetur.</p>
        </div>
        <div class="formalization">
          <p class="number">05</p>
          <h5>Continuity formalization</h5>
          <p>Lorem ipsum dolor sit amet consectetur.</p>
        </div>
      </div>
    </div>
    <!-- /.process -->
  </div>
  <!-- /.management -->
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.management {
  padding: 120px 0;
  color: #66737b;
  font-weight: 300;
  text-align: center;

  h3 {
    color: $nexgen_text_dark;

    .title_bg {
      background-color: #daeced;
      color: $nexgen_primary_green;
    }
  }

  .info_text {
    width: 40%;
    margin: auto;
  }

  .process {
    margin-top: 5rem;
    border-top: 5px solid #daeced;

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
        color: $nexgen_primary_green;
      }

      h5 {
        color: $nexgen_text_dark;
        margin: 1rem 0;
        line-height: 1.8rem;
      }
    }
  }
}
</style>