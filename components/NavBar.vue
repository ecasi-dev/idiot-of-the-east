<template>
  <nav class="nav-bar">
    <ul>
      <li>
        <a href="#">
          <img
            src="https://i2.lensdump.com/i/tzKEc3.webp"
            alt="Home"
            class="home-icon"
          />
        </a>
      </li>
      <li>
        <a href="">
          <img src="https://i3.lensdump.com/i/tzK6g0.webp" alt="navigation" class="hamburger-icon"/>
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.nav-bar {
  background-color: #858585;
  padding: 0 6vw;
  border-top: 1px solid black;
  border-bottom: 1px solid black;

  ul {
    list-style-type: none;
    display: flex;
    justify-content: space-between;
    align-items: center;

    a {
      text-decoration: none;
      color: black;

      .home-icon {
        height: 45px;
        display: block;
      }

      .hamburger-icon{
        height: 45px;
        display: block;
      }
    }
  }
}
</style>
