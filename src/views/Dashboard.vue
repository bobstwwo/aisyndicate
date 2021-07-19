<template>
  <div class="dashboard">
    <header class="header">
      <div class="logo">
        <logo />
      </div>
      <div class="exit">
        <div class="exit__icon">X</div>
        <div class="exit__text">Вход</div>
      </div>
    </header>
    <main class="main">
      <div class="main__left">
        <div class="title"><h1>Личный кабинет</h1></div>
        <div class="profile-image"><span>Д</span></div>
        <div class="user-name"><span>Даниил Волков</span></div>
        <div class="menu">
          <ul>
            <li class="li-active">Мои стартапы</li>
            <li>Инвестиции</li>
            <li class="add-border">Мои голоса</li>
            <li class="add-padding">Кошелек</li>
            <li class="add-border">Платные услуги</li>
            <li class="add-padding">Настройки аккаунта</li>
          </ul>
        </div>
      </div>
      <div class="main__right">
        <div class="main__right-title"><span>Мои стартапы</span></div>
        <div class="empty">
          <div class="box df"><img src="@/assets/images/box.png" alt="" /></div>
          <div class="empty-title df"><span>Пока пусто</span></div>
          <div class="empty-text df">
            <span>Здесь появятся ваши стартапы после создания</span>
          </div>
        </div>
      </div>
    </main>
    <footer class="footer">
      <div class="footer__logo mr"><logo /></div>
      <div class="footer__about mr">
        <div class="footer-title">ABOUT</div>
        <div>
          <ul>
            <li>About Us</li>
            <li>Privacy Policy</li>
            <li>FAQs</li>
            <li>Contacts</li>
          </ul>
        </div>
      </div>
      <div class="footer__support mr">
        <div class="footer-title">SUPPORT</div>
        <div>
          <ul>
            <li>Help Center</li>
            <li>Our Rules</li>
            <li>Creator Resources</li>
          </ul>
        </div>
      </div>
      <div class="footer__more mr">
        <div class="footer-title">MORE FROM AI SYNDICATE</div>
        <div>
          <ul>
            <li>Meet The Team</li>
          </ul>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import Logo from '@/components/Images/Logo.vue';
export default {
  name: 'Home',
  components: {
    Logo,
  },
};
</script>

<style lang="scss" scoped>
* {
  font-family: 'Red Rose';
}
.dashboard {
  height: 100vh;
}
.main {
  display: flex;
  &__left {
    width: 30%;
    border-right: 1px solid #8b8b8b;
  }
  &__right {
    width: 70%;
  }
}
.empty-text {
  font-family: Roboto;
  font-size: 27px;
  line-height: 32px;
  color: #000000;
}
.df {
  display: flex;
  align-items: center;
  justify-content: center;
}
.empty-title {
  font-family: Roboto;
  font-weight: 500;
  font-size: 32px;
  line-height: 37px;
  color: #000000;
}

.main__right {
  position: relative;
}
.main__right-title {
  margin: 18px 34px;
  & span {
    font-family: Roboto;
    font-size: 32px;
    line-height: 37px;
    color: #000000;
  }
}
.menu {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
  & ul {
    list-style-type: none;
    & li {
      font-family: Roboto;
      font-size: 22px;
      line-height: 26px;
      color: #000000;
      display: block;
    }
  }
}
.li-active {
  background: #dedede;
  padding: 3px;
  border-radius: 15px;
}
.add-border {
  border-bottom: 1px solid #8b8b8b;
  padding-bottom: 10px;
}
.add-padding {
  padding-top: 10px;
}
.user-name {
  display: flex;
  justify-content: center;
  margin: 11px 0;
  & span {
    font-family: Roboto;
    font-weight: bold;
    font-size: 28px;
    line-height: 33px;
    color: #000000;
    border-bottom: 1px solid #8b8b8b;
  }
}
.profile-image {
  width: 153px;
  height: 153px;
  background: #f4ce04;
  border-radius: 50%;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: center;
  & span {
    font-family: Roboto;
    font-size: 72px;
    line-height: 84px;
    color: #000000;
  }
}
.title {
  display: flex;
  justify-content: center;
  margin: 18px 0;
}
.header {
  display: flex;
  justify-content: center;
  position: relative;
  border-bottom: 1px solid black;
}
.exit {
  position: absolute;
  right: 81px;
  top: 50%;
  transform: translate(0, -50%);
  display: flex;
  &__icon {
    margin-right: 20px;
  }
}
.footer {
  padding: 41px 32px;
  background: #e0e0e0;

  display: flex;
  align-items: flex-start;
  & ul {
    list-style-type: none;
    & li {
      &:hover {
        cursor: pointer;
      }
    }
  }
}
.footer-title {
  font-weight: bold;
  font-size: 15px;
  line-height: 19px;
  color: #000000;
}
.mr {
  margin-right: 40px;
}
</style>
