<template>
  <header>
    <div class="nav-container">
      <div class="navbar">
        <div class="navbar-title">
          <button
            @click="btnAnimate"
            class="burger"
            :class="{ active: isActive }"
          >
            <span></span>
          </button>
          <img src="../assets/img/emojione-v1_movie-camera.svg" alt="" />
        </div>
        <div class="search">
          <input type="text" />
          <button>
            <span
              ><img src="../assets/img/bi_arrow-right-circle.svg" alt=""
            /></span>
          </button>
        </div>
      </div>
      <hr />
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    btnAnimate() {
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style lang="scss">
header {
  .nav-container {
    width: 100%;
    padding: 0 25px;
    margin-right: auto;
    margin-left: auto;
    .navbar {
      display: flex;
      align-items: flex-end;
      .navbar-title {
        display: flex;
        .burger {
          cursor: pointer;
          width: 60px;
          outline: none;
          border: none;
          background: transparent;
          margin-top: 24px;
          span,
          ::after,
          ::before {
            width: 30px;
            height: 3px;
            background-color: #fff;
            display: block;
            transition: all 0.15s ease;
            content: "";
          }
          span::after {
            transform: translateY(-11px);
          }
          span::before {
            transform: translateY(8px);
          }
          &.active ::before {
            transform: rotate(45deg) translate(3px, 2px);
          }
          &.active span {
            background: transparent;
          }
          &.active ::after {
            transform: rotate(-45deg);
          }
        }
      }
      .search {
        display: flex;
        width: 50%;
        input {
          background: #444444;
          border: 1px solid #333333;
          box-sizing: border-box;
          border-radius: 52px;
          outline: none;
          width: 100%;
          height: 53px;
          padding-inline-start: 44px;
          font-family: "Poppins", sans-serif;
          input[textarea] {
            color: white;
          }
        }

        button {
          outline: none;
          border: none;
          background: transparent;
        }
      }
    }
    hr {
      background: #fff;
    }
  }
}
</style>
