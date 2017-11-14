<template>
  <footer>
    <div class="container">
      <div class="footer__content">
        <div class="footer__content__links">
          <nav>
            <h3>Programs &amp; initiatives</h3>
            <ul>
              <li><a href="#">TEDx</a></li>
              <li><a href="#">TED Prize</a></li>
              <li><a href="#">TED Fellows</a></li>
              <li><a href="#">TED Ed</a></li>
              <li><a href="#">TED Translators</a></li>
              <li><a href="#">TED Books</a></li>
              <li><a href="#">TED Institute</a></li>
            </ul>
          </nav>
          <nav>
            <h3>Ways to get TED</h3>
            <ul>
              <li><a href="#">TED Radio Hour on NPR</a></li>
              <li><a href="#">More ways to get TED</a></li>
            </ul>
          </nav>
          <nav>
            <h3>Follow TED</h3>
            <ul>
              <li><a href="#">Facebook</a></li>
              <li><a href="#">Twitter</a></li>
              <li><a href="#">Google+</a></li>
              <li><a href="#">Pinterest</a></li>
              <li><a href="#">Instagram</a></li>
              <li><a href="#">YouTube</a></li>
              <li><a href="">TED Blog</a></li>
            </ul>
          </nav>
          <nav>
            <h3>Our community</h3>
            <ul>
              <li><a href="#">TED Speakers</a></li>
              <li><a href="#">TED Fellows</a></li>
              <li><a href="#">TED Translators</a></li>
              <li><a href="#">TEDx Organizers</a></li>
              <li><a href="#">TED Community</a></li>
            </ul>
          </nav>
        </div>
        <div class="footer__content__forms">
          <form>
            <h3>Get TED email updates</h3>
            <div>
              <p>Subscribe to receive email notificationswhenever new talks are published.</p>
              <div class="footer-newsletter__options">
                <div class="footer-newsletter__option">
                  <label><input checked="" name="subscription[list][]" type="checkbox" value="daily">Daily</label>
                </div>
                <div class="footer-newsletter__option">
                  <label><input name="subscription[list][]" type="checkbox" value="weekly">Weekly</label>
                </div>
              </div>
              <div class="form-group">
                <label for="newsletter-signup-email">Your email address</label>
                <input class="form-control" id="newsletter-signup-email" name="subscription[email]" size="16">
              </div>
              <button>Submit</button>
            </div>
          </form>
        </div>
      </div>
    </div>
    <div class="footer__services">
      <div class="container footer__services__container">
        <nav role="navigation">
          <ul class="footer__links">
            <li><a href="#">TED Talks Usage Policy</a></li>
            <li><a href="#">Privacy Policy</a></li>
            <li><a href="#">Advertising / Partnership</a></li>
            <li><a href="#">TED.com Terms of Use</a></li>
            <li><a href="#">Contact</a></li>
            <li><a href="#">Jobs</a></li>
            <li><a href="#">Press</a></li>
            <li><a href="#">Help</a></li>
          </ul>
        </nav>
        <p class="footer__service--info" role="contentinfo">© TED Conferences, LLC</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'app-footer'
}
</script>

<style lang="scss" scoped>
footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  border-top: 2px solid #E62B1E;
}
.container {
  max-width: 1200px;
  width: 100%;
}
.footer__content, .footer__content__links {
  display: flex;
}
h3 {
  height: 40px;
}
a:hover {
  text-decoration: underline;
}
.footer__content {
  padding: 40px 0;
  font-size: 13px;
  .footer__content__links {
    flex: 0 0 70%;
    &>* {
      flex: 0 0 25%;
      padding: 0 18px;
    }
    a {
      color: #888;
      line-height: 1.8;
      &:hover { color: black; }
    }
  }
  .footer__content__forms {
    flex: 0 0 30%;
    padding: 0 40px;
    border-left: 1px solid #eee;
    .footer-newsletter__options {
      display: flex;
      padding: 20px 0;
      .footer-newsletter__option {
        margin-right: 30px;
        input {
          margin-right: 6px;
        }
      }
    }
    .form-group {
      display: flex;
      flex-direction: column;
      input {
        margin-top: 4px;
        border-radius: 4px;
        display: inline-block;
        background: #FFF;
        border: 1px solid #DDD;
        color: #333;
        font-size: 16px;
        height: 40px;
        padding: 10px;
        width: 100%;
      }
    }
    button {
      color: #444;
      margin-top: 20px;
      background-color: #F5F5F5;
      background-image: linear-gradient(#F5F5F5,#E6E6E6);
      border-radius: 3px;
      display: inline-block;
      vertical-align: middle;
      border: 1px solid #CCC;
      cursor: pointer;
      font-size: 14px;
      font-weight: 700;
      line-height: 24px;
      padding: 7px 30px;
      text-decoration: none;
      text-shadow: 0 1px 0 #fff;
    }
  }
}
.footer__services {
  display: flex;
  justify-content: center;
  align-self: stretch;
  background: black;
  padding: 10px;
  color: white;
  font-size: 12px;
  .footer__links, .footer__services__container {
    display: flex;
  }
  .footer__services__container {
    justify-content: space-between;
    .footer__service {

    }
  }
  li + li {
    margin-left: 20px;
  }
}
</style>