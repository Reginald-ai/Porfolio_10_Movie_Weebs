<template>
  <div class="aside-navbar col-md-2">
    <ul class="navbar-nav">
      <li class="nav-item">
        <a href="#" class="nav-link"
          ><span><img src="../assets/img/carbon_home.svg" alt=""/></span>
          Home</a
        >
      </li>
    </ul>
    <hr />
    <ul class="navbar-nav">
      <li class="navbar-item">
        <a class="nav-link" href="#">Rating Highest</a>
      </li>
      <li class="navbar-item">
        <a class="nav-link" href="#">Rating Lowest</a>
      </li>
      <li class="navbar-item"><a class="nav-link" href="#">Year New</a></li>
      <li class="navbar-item">
        <a class="nav-link" href="#">Year Oldset</a>
      </li>
    </ul>
    <hr />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.aside-navbar {
  color: white;
  width: 240px;
  // position: absolute;
  // top: 105px;
  // left: 0px;
  // bottom: 0;
  display: block;

  .navbar-nav {
    padding: 1rem 1rem;
    .nav-item {
      display: flex;
      align-items: center;
    }
    .nav-link {
      color: #fff;
      display: flex;
      align-items: center;
      padding: 15px;
      border-radius: 5px;
      &:hover {
        background: rgba(255, 255, 255, 0.1);
        width: 100%;
      }
      span {
        margin-right: 10px;
      }
    }
  }
}
.opens {
  display: none;
}
</style>
