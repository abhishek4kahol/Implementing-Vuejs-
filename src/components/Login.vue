<template>
<div class="login-wrapper columns">
  <div class="column is-8 is-hidden-mobile hero-banner">
    <section class="hero is-fullheight is-dark">
      <div class="hero-body">
        <div class="container section">
          <div class="has-text-right">
            <h1 class="title is-1">Login</h1> <br>
            <p class="title is-3 quote">{{twitterQuote}}</p>
          </div>
        </div>
      </div>
      <div class="hero-footer">
        <p class="has-text-centered">Image via unsplash</p>
      </div>
    </section>
  </div>
  <div class="column is-4">
    <section class="hero is-fullheight">
      <div class="hero-heading">
        <div class="section has-text-centered">
          <img src="http://bulma.io/images/bulma-logo.png" alt="Bulma logo" width="150px">
        </div>
      </div>
      <div class="hero-body">
        <div class="container">
          <div class="columns">
            <div class="column is-9 is-offset-2">
              <h1 class="avatar has-text-centered section">
                    <img src="https://placehold.it/128x128">
                  </h1>
              <div class="login-form">
                <p class="control has-icon has-icon-right">
                  <input class="input email-input" type="text" placeholder="jsmith@example.org">
                  <span class="icon user">
                        <i class="fa fa-user"></i>
                      </span>
                </p>
                <p class="control has-icon has-icon-right">
                  <input class="input password-input" type="password" placeholder="●●●●●●●">
                  <span class="icon password">
                        <i class="fa fa-lock"></i>
                      </span>
                </p>
                <p class="control login">
                  <button class="button is-success is-outlined is-large is-fullwidth">Login</button>
                </p>
              </div>
              <div class="section forgot-password">
                <p class="has-text-centered">
                  <a href="#">Forgot password</a>
                  <a href="#">Help?</a>
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</div>
</template>
<script>
export default {
  name: 'Login',
  // components: {
  //   Icon
  // }
  data () {
    return {
      twitterQuote: 'You have to dream before your dreams can come true.'
    }
  },
  mounted: function () {
    for (var k = 0; k < 100; k++) {
      // setTimeout(this.newQuote(), 2000) // this method will execute at pageload
      setTimeout(function () { this.newQuote() }.bind(this), 2000)
    }
  },
  methods: {
    newQuote: function () {
      console.log('here')
      var quotesArr = ['If you are going through hell, keep going.',
        'You have to dream before your dreams can come true.',
        'Everyday life is like programming,I guess. If you love something you can put beauty into it.', 'Experience is the name everyone gives to their mistakes.', 'It’s kind of fun to do the impossible.', 'Knowledge is power. '
      ]
      // var authorArr = ['Sir Winston Churchill',
      //   'A.P.J.Abdul Kalam',
      //   'Donald Knuth',
      //   'Oscar Wilde',
      //   'Walt Disney',
      //   'Francis Bacon'
      // ]
      // var pageColor = ['#66ff99', '#ff3333', '#c6ff1a', '#33cccc', '#8080f', '#cc00cc', '#669999', '#1aff1a']
      // console.log('up', quotesArr)
      for (var j = 0; j < 10; j++) {
        var i = Math.floor(Math.random() * quotesArr.length)
        // console.log('i is', i)
        // document.getElementByclass('quote').innerHTML = quotesArr[i]
        // document.getElementById('quote-author').innerHTML = authorArr[i]
        // document.getElementById('quote-box').style.backgroundColor = pageColor[i]
        this.twitterQuote = quotesArr[i] // + ' ' + ' ' + authorArr[i]
      }
    }
  }
}
</script>
<style>
/*html,body {
  font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
  height: 100%;
  padding: 0;
  margin: 0;
}*/

.email-input,
.password-input {
  border-radius: 40px;
  font-size: 20px;
  padding-left: 15px;
  color: #95A5A6;
}

.icon.user,
.icon.password {
  margin: 18px 10px 0 0;
}

.avatar img {
  border-radius: 100px;
  padding: 5px;
  border: 1px solid #dbdbdb;
}

.forgot-password a {
  color: #95A5A6;
  font-weight: bold;
  padding-right: 20px;
}

.control {
  padding-top: 12px;
}

.login {
  padding-top: 23px;
}

.login button {
  border-radius: 40px;
  font-weight: bold;
}

.hero-body .container {
  margin-top: -100px;
}

.hero.is-dark .section {
  background-color: transparent;
}

.login-wrapper {
  margin: -0.75rem;
  overflow-y: hidden;
}

.hero-banner .hero {
  background: url('https://unsplash.it/2000/1000');
  background-position: center;
  background-size: cover;
  background-blend-mode: screen;
}

.hero-banner .title {
  display: inline-block;
  background-color: rgba(0, 0, 0, 0.6);
  padding: 5px;
}
</style>
