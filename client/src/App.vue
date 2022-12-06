<template>
  <div>
    <header id="header" class="">
      <section id="navTop" class="nav-top py-2 d-none d-md-block">
        <div class="container">
          <div class="row align-items-center justify-content-center">
            <div class="col-4"></div>
            <div class="col-4 logo">
              <img src="https://img.freepik.com/premium-vector/company-logo-design-ideas-vector-free-vector_536813-247.jpg?w=1380" class="rounded mx-auto d-block" alt="" style="height: 150px;">
            </div>
            <div class="col-4 text-end socials">
              <div class="sign-container">
                <li v-if="user.email==undefined"><a type="button" class="login" @click="kakaoLogin" style="color:black">Kakao-Login</a></li>
                <!-- <li v-if="user.email==undefined"><button class="btn btn-danger" type="button" @click="kakaoLogin">로그인</button></li> -->
                <!-- <li v-else><button class="btn btn-danger" type="button" @click="kakaoLogout">로그아웃</button></li> -->
                <li v-else><a type="button" class="logout" @click="kakaoLogout" style="color:black">Logout</a></li>
              </div>
            </div>
          </div>
        </div>
      </section>

      <nav id="navPrimary" class="navbar navbar-expand-md bg-dark">
        <div class="container-xxl">
          <a class="navbar-brand d-block d-md-none" href="index.html">
            <!-- <img src="https://img.freepik.com/premium-vector/company-logo-design-ideas-vector-free-vector_536813-247.jpg?w=1380" class="rounded mx-auto d-block" alt="" style="height: 50px;"> -->
          </a>
          <div class="collapse navbar-collapse" id="navPrimaryContent">
              <ul class="navbar-nav mx-auto mb-2 mb-lg-0">
                <li class="nav-item">
                  <router-link class="nav-link " style="color:white" to="/" >Home</router-link>
                </li>
                <li class="nav-item dropdown">
                  <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false" style="color:white">
                    Intro
                  </a>
                  <ul class="dropdown-menu">
                    <li><a class="dropdown-item" href="page.html">About us</a></li>
                    <li><a class="dropdown-item" href="page.html">Find us</a></li>
                  </ul>
                </li>
                <li class="nav-item">
                  <router-link class="nav-link active" style="color:white" to="/">List</router-link>
                </li>
                <li class="nav-item">
                  <router-link class="nav-link" to="/detail" style="color:white">Item-Detail</router-link>
                </li>
                <li class="nav-item">
                  <router-link class="nav-link" to="/sales" style="color:white">Item-Register</router-link>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="page.html" style="color:white">SHITRS</a>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="page.html" style="color:white">PANTS</a>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="page.html" style="color:white">SALE</a>
                </li>
                <!-- <li class="nav-item">
                  <a class="nav-link btn btn-outline-secondary" href="#"><i class="fa fa-search"></i></a>
                </li> -->
              </ul>
            </div>
            <!-- 토글버튼 -->
            <button class="btn btn-outline-secondary d-block d-md-none" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasRight" aria-controls="offcanvasRight">
              <span class="navbar-toggler-icon">ㅡ</span>
            </button>
            <!-- 오른쪽 상단 메뉴 표시 -->
            <div class="offcanvas offcanvas-end d-block d-md-none" data-bs-scroll="true" tabindex="-1" id="offcanvasRight" aria-labelledby="offcanvasRightLabel">
              <div class="offcanvas-header">
                <h5 class="offcanvasRightLabel">Menu</h5>
                <button class="btn-close text-reset" type="button" data-bs-dismiss="offcanvas" aria-label="Close"></button>
              </div>
              <div class="offcanvas-body">
                <ul class="list-unstyled mobile-menu">
                  <li><a href="index.html" class="text-decoration-none link-dark active">Home</a></li>
                  <li>
                    <a href="page.html" class="text-decoration-none link-dark">Intro</a>
                    <ul class="list-unstyled ms-3">
                      <li><a href="page.html" class="text-decoration-none link-dark">About us</a></li>
                      <li><a href="page.html" class="text-decoration-none link-dark">Find us</a></li>
                    </ul>
                  </li>
                  <li><a href="page.html" class="text-decoration-none link-dark"></a></li>
                  <li><a href="page.html" class="text-decoration-none link-dark">BEST</a></li>
                  <li><a href="page.html" class="text-decoration-none link-dark">NEW</a></li>
                  <li><a href="page.html" class="text-decoration-none link-dark">OUTER</a></li>
                  <li><a href="page.html" class="text-decoration-none link-dark">SHIRTS</a></li>
                  <li><a href="page.html" class="text-decoration-none link-dark">PANTS</a></li>
                  <li><a href="page.html" class="text-decoration-none link-dark">SALE</a></li>
                  <li><a href="#" class="btn btn-outline-secondary w-100"><i class="fa fa-search"></i></a></li>
                </ul>
              </div>
            </div>
        </div>
      </nav>
    </header>
    
    
  <!-- <section id="carouselExampleCaptions" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-indicators">
      <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
      <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
      <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" aria-label="Slide 3"></button>
    </div>
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F996333405A8280FC23" class="d-block w-100" alt="...">
        <div class="carousel-caption d-none d-md-block">
          <h5>First slide label</h5>
          <p>Some representative placeholder content for the first slide.</p>
        </div>
      </div>
      <div class="carousel-item">
        <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F9962DE405A8280FD23" class="d-block w-100" alt="...">
        <div class="carousel-caption d-none d-md-block">
          <h5>Second slide label</h5>
          <p>Some representative placeholder content for the second slide.</p>
        </div>
      </div>
      <div class="carousel-item">
        <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F99BE8A405A8280FD19" class="d-block w-100" alt="...">
        <div class="carousel-caption d-none d-md-block">
          <h5>Third slide label</h5>
          <p>Some representative placeholder content for the third slide.</p>
        </div>
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </section> -->
  <router-view/>
  <footer class="mt-5 py-5 bg-dark">
            <div class="row">
              <div class="col-12 col-md">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="d-block mb-2" role="img" viewBox="0 0 24 24"><title>Product</title><circle cx="12" cy="12" r="10"/><path d="M14.31 8l5.74 9.94M9.69 8h11.48M7.38 12l5.74-9.94M9.69 16L3.95 6.06M14.31 16H2.83m13.79-4l-5.74 9.94"/></svg>
                <small class="d-block mb-3 text-muted">&copy; 2017–2021</small>
              </div>
              <div class="col-6 col-md">
                <h5>Features</h5>
                <ul class="list-unstyled text-small">
                  <li><a class="link-secondary" href="#">Cool stuff</a></li>
                  <li><a class="link-secondary" href="#">Random feature</a></li>
                  <li><a class="link-secondary" href="#">Team feature</a></li>
                  <li><a class="link-secondary" href="#">Stuff for developers</a></li>
                  <li><a class="link-secondary" href="#">Another one</a></li>
                  <li><a class="link-secondary" href="#">Last time</a></li>
                </ul>
              </div>
              <div class="col-6 col-md">
                <h5>Resources</h5>
                <ul class="list-unstyled text-small">
                  <li><a class="link-secondary" href="#">Resource name</a></li>
                  <li><a class="link-secondary" href="#">Resource</a></li>
                  <li><a class="link-secondary" href="#">Another resource</a></li>
                  <li><a class="link-secondary" href="#">Final resource</a></li>
                </ul>
              </div>
              <div class="col-6 col-md">
                <h5>Resources</h5>
                <ul class="list-unstyled text-small">
                  <li><a class="link-secondary" href="#">Business</a></li>
                  <li><a class="link-secondary" href="#">Education</a></li>
                  <li><a class="link-secondary" href="#">Government</a></li>
                  <li><a class="link-secondary" href="#">Gaming</a></li>
                </ul>
              </div>
              <div class="col-6 col-md">
                <h5>About</h5>
                <ul class="list-unstyled text-small">
                  <li><a class="link-secondary" href="#">Team</a></li>
                  <li><a class="link-secondary" href="#">Locations</a></li>
                  <li><a class="link-secondary" href="#">Privacy</a></li>
                  <li><a class="link-secondary" href="#">Terms</a></li>
                </ul>
              </div>
            </div>
          </footer>
          </div>
</template>
<script>
export default {
  computed: {
    user() {
      return this.$store.state.user;
    }
  },
  methods: {
    kakaoLogin() {
      window.Kakao.Auth.login({
        scope: 'profile_nickname, account_email, gender',
        success: this.getProfile
      });
    },
    getProfile(authObj) {
      console.log(authObj);
      window.Kakao.API.request({
        url: '/v2/user/me',
        success: res => {
          const kakao_account = res.kakao_account;
          console.log(kakao_account);
          this.login(kakao_account);
          alert("로그인 성공");
        }
      });
    },
    async login(kakao_account) {
      await this.$api("/api/login", {
        param: [
          {email:kakao_account.email, nickname:kakao_account.profile_nickname},
          {nickname:kakao_account.profile_nickname}
        ]
      });
      this.$store.commit("user", kakao_account);
    },
    kakaoLogout() {
      window.Kakao.Auth.logout((response) => {
        console.log(response);
        this.$store.commit("user", {});
        alert("로그아웃");
        this.$router.push({path:'/'});

      });
    }
  }
}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
} */
@font-face {
    font-family: 'LINESeedKR-Bd';
    src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_11-01@1.0/LINESeedKR-Bd.woff2') format('woff2');
    font-weight: 700;
    font-style: normal;
}
@font-face {
    font-family: 'MICEGothic Bold';
    src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2206-01@1.0/MICEGothic Bold.woff2') format('woff2');
    font-weight: 700;
    font-style: normal;
}

.login {
  font-family: 'LINESeedKR-Bd';
  font-size: 1.3rem;
}

.logout {
  font-family: 'LINESeedKR-Bd';
  font-size: 1.3rem;
}

.nav-link {
  font-family: 'MICEGothic Bold';
  font-size: 1rem;
}

.nav-link active {
  font-family: 'MICEGothic Bold';
  font-size: 1rem;
}

/* 토글버튼 안 글씨 */
.text-decoration-none {
  font-family: 'MICEGothic Bold';
}

/* 슬라이드  */
.carousel {
  margin-top: 2.5rem;
  margin-bottom: 2.5rem;
  margin-right: 2rem;
  margin-left: 2rem;
  border-radius: 1rem;
}

.carousel .carousel-inner {
  border-radius: 1rem;
  box-shadow: 0 16px 24px 2px rgba(0, 0, 0, 0.14), 0 6px 30px 5px rgba(0, 0, 0, 0.12), 0 8px 10px -5px rgba(0, 0, 0, 0.2);
}



</style>
