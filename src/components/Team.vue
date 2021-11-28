<template>
  <div class="team">
    <div class="container">
      <div class="d_flex">
        <div class="left">
          <p class="section_title">{{ sectionTitle }}</p>
          <h2>
            <span class="title_bg">{{ title.marked }}</span>
            {{ title.notMarked }}
          </h2>
          <p>
            {{ description }}
          </p>
          <p>{{ information }}</p>
          <div class="team_members d_flex">
            <div
              class="team_member d_flex"
              v-for="(person, i) in teamMembers"
              :key="i"
            >
              <img :src="person.picture.url" :alt="person.name" />
              <div class="info">
                <h4>{{ person.name }}</h4>
                <p>{{ person.role }}</p>
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
          </div>
          <!-- /.team_members -->
        </div>

        <div class="right speech">
          <h4>President Speech</h4>
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
export default {
  data() {
    return {
      sectionTitle: "We like what we do",
      title: {
        marked: "Team",
        notMarked: "of Experts",
      },
      description: `Ethics and integrity are the bases on whici our professionals build
            their careers.`,
      information: `They are fundamentals that become daily attitudes.`,
      teamMembers: [
        {
          picture: { url: require("../assets/img/team-1.jpg") },
          name: "David Cooper",
          role: "CTO & CO-FOUNDER",
        },
        {
          picture: { url: require("../assets/img/team-2.jpg") },
          name: "Emma Lopez",
          role: "chief marketing",
        },
        {
          picture: { url: require("../assets/img/team-3.jpg") },
          name: "Oliver Jones",
          role: "chief procurement",
        },
        {
          picture: { url: require("../assets/img/team-4.jpg") },
          name: "T. Johnson",
          role: "ceo & president",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.team {
  background-color: $nexgen_primary_dark;
  padding: 130px 0;
  color: $nexgen_light_grey_text;
  font-weight: 300;

  & > .container > .d_flex {
    align-items: flex-end;
  }

  .left {
    width: 70%;

    h2 {
      color: $nexgen_white;

      .title_bg {
        background-color: rgba($nexgen_primary_color, 0.2);
      }
    }

    .d_flex {
      margin-top: 2rem;
      justify-content: flex-start;
    }

    .team_members {
      &.d_flex {
        flex-wrap: wrap;
      }

      .team_member {
        justify-content: flex-start;
        align-items: flex-end;

        img {
          width: 110px;
          border-radius: 5px;
          margin-right: 2rem;
        }

        .info {
          width: 170px;
          margin-right: 4rem;

          h4 {
            color: $nexgen_white;
          }

          p {
            font-size: 0.9rem;
            text-transform: uppercase;
            padding: 0.5rem 0 1rem 0;
          }

          .social {
            .social_icon {
              transition: 0.5s ease-in-out;
              display: flex;
              justify-content: center;
              align-items: center;
              width: 40px;
              height: 40px;
              background-color: rgba($nexgen_primary_color, 0.2);
              border-radius: 50%;
              color: $nexgen_primary_color;
              font-size: 1rem;
              cursor: pointer;

              &:hover {
                background-color: $nexgen_primary_color;
                color: $nexgen_white;
              }
            }
          }
        }

        .social.d_flex {
          margin: 0;
          gap: 0.3rem;
        }
      }
    }
  }

  .right.speech {
    width: 30%;
    background-color: $nexgen_primary_color;
    border-radius: 5px;
    padding: 2rem 1.8rem 2rem 2rem;
    color: $nexgen_white;

    p {
      margin: 1.5rem 0;
    }

    .icon {
      color: rgba($nexgen_black, 25%);
      font-size: 1.5rem;
    }
  }
}
</style>