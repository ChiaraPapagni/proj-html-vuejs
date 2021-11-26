<template>
  <div class="team">
    <div class="container">
      <p class="section_title">We like what we do</p>
      <div class="d_flex">
        <div class="experts">
          <h3><span class="title_bg">Team</span> of Experts</h3>
          <p>
            Ethics and integrity are the bases on whici our professionals build
            their careers.
          </p>
          <p>They are fundamentals that become daily attitudes.</p>

          <div class="d_flex">
            <div class="team_member d_flex">
              <img src="../assets/img/team-1.jpg" alt="David Cooper" />
              <div class="info">
                <h5>David Cooper</h5>
                <p>cto & co-founder</p>
                <div class="social d_flex">
                  <div class="social_icon">
                    <font-awesome-icon :icon="['fab', 'facebook-f']" />
                  </div>
                  <div class="social_icon">
                    <font-awesome-icon :icon="['fab', 'twitter']" />
                  </div>
                  <div class="social_icon">
                    <font-awesome-icon :icon="['fab', 'linkedin-in']" />
                  </div>
                </div>
              </div>
            </div>
            <!-- /.team_member -->

            <div class="team_member d_flex">
              <img src="../assets/img/team-2.jpg" alt="Oliver Jones" />
              <div class="info">
                <h5>Oliver Jones</h5>
                <p>chief procurement</p>
                <div class="social d_flex">
                  <div class="social_icon">
                    <font-awesome-icon :icon="['fab', 'facebook-f']" />
                  </div>
                  <div class="social_icon">
                    <font-awesome-icon :icon="['fab', 'twitter']" />
                  </div>
                  <div class="social_icon">
                    <font-awesome-icon :icon="['fab', 'linkedin-in']" />
                  </div>
                </div>
              </div>
            </div>
            <!-- /.team_member -->

            <div class="team_member d_flex">
              <img src="../assets/img/team-3.jpg" alt="Emma Lopez" />
              <div class="info">
                <h5>Emma Lopez</h5>
                <p>chief marketing</p>
                <div class="social d_flex">
                  <div class="social_icon">
                    <font-awesome-icon :icon="['fab', 'facebook-f']" />
                  </div>
                  <div class="social_icon">
                    <font-awesome-icon :icon="['fab', 'twitter']" />
                  </div>
                  <div class="social_icon">
                    <font-awesome-icon :icon="['fab', 'linkedin-in']" />
                  </div>
                </div>
              </div>
            </div>
            <!-- /.team_member -->

            <div class="team_member d_flex">
              <img src="../assets/img/team-4.jpg" alt="T. Johnson" />
              <div class="info">
                <h5>T. Johnson</h5>
                <p>ceo & president</p>
                <div class="social d_flex">
                  <div class="social_icon">
                    <font-awesome-icon :icon="['fab', 'facebook-f']" />
                  </div>
                  <div class="social_icon">
                    <font-awesome-icon :icon="['fab', 'twitter']" />
                  </div>
                  <div class="social_icon">
                    <font-awesome-icon :icon="['fab', 'linkedin-in']" />
                  </div>
                </div>
              </div>
            </div>
            <!-- /.team_member -->
          </div>
        </div>
        <!-- /.experts -->

        <div class="speech">
          <h5>President Speech</h5>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesent
            ut lacinia diam.
          </p>
          <p>
            Vivamus efficitur et est quis posuere. Nulla sollicitudin vulputate
            dui, id pretium torto congue eu. Integer aliquet justo eu quam
            volutpat ullamcorper.
          </p>
          <p>
            Duis ut hendrerit mauris. Phasellus faucibus ut enim vel tincidunt.
            Nunc venanatis a dui el laoreet.
          </p>
          <div class="speech_footer d_flex">
            <strong>T. Jhonson</strong>
            <font-awesome-icon :icon="['fas', 'quote-right']" class="icon" />
          </div>
        </div>
        <!-- /.speech -->
      </div>
    </div>
  </div>
  <!-- /.team -->
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.team {
  background-color: $nexgen_bg_dark;
  padding: 120px 0;
  color: #ccc;
  font-weight: 300;

  & > .container > .d_flex {
    align-items: flex-end;
  }

  .experts {
    width: 68%;

    h3 {
      color: white;

      .title_bg {
        background-color: #0e272d;
      }
    }

    .d_flex {
      margin-top: 3rem;
      justify-content: flex-start;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .team_member {
      &.d_flex {
        margin-top: 1rem;
      }

      justify-content: flex-start;

      img {
        width: 110px;
        border-radius: 5px;
        margin-right: 1rem;
      }

      .info {
        width: 160px;
        margin-right: 2rem;

        h5 {
          color: white;
        }

        p {
          font-size: 0.9rem;
          text-transform: uppercase;
          padding: 0.5rem 0 1rem 0;
        }

        .social {
          .social_icon {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 40px;
            height: 40px;
            background-color: #0e272d;
            border-radius: 50%;
            color: $nexgen_primary_green;
            font-size: 1rem;
          }
        }
      }

      .social.d_flex {
        margin: 0;
        gap: 0.3rem;
      }
    }
  }

  .speech {
    width: 32%;
    background-color: $nexgen_primary_green;
    border-radius: 5px;
    padding: 2rem 1.8rem 2rem 2rem;
    color: white;

    p {
      margin: 1.5rem 0;
    }

    .icon {
      color: #046162;
      font-size: 1.2rem;
    }
  }
}
</style>