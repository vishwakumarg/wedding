<template>
  <div>
    <div class="gla_page_loader gla_image_bck">
      <div class="gla_loader">
        <p>
          <img
            src="./images/animations/wedding.gif"
            height="150"
            alt
          >
        </p>
        <p>
          <img
            src="./images/logo.png"
            height="150"
            alt
          >
        </p>
        <p style="color:aliceblue">Loading...</p>
      </div>
    </div>

    <div class="gla_page" id="gla_page">
      <a href="#gla_page" class="gla_top ti ti-angle-up gla_go"></a>
      <header>
        <nav class="gla_light_nav gla_transp_nav">
          <div class="container">
            <div class="gla_logo_container clearfix">
              <div class="gla_logo_txt">
                <a v-bind:href="'/'" class="gla_logo">Swapnil & Priyanka</a>
                <div class="gla_logo_und">December 18, 2022</div>
              </div>
            </div>

            <div class="gla_main_menu gla_main_menu_mobile">
              <div class="gla_main_menu_icon">
                <i></i>
                <i></i>
                <i></i>
                <i></i>
                <b>Menu</b>
                <b class="gla_main_menu_icon_b">Back</b>
              </div>
            </div>

            <div class="gla_main_menu_content gla_image_bck" data-image="./static/menu.jpg">
              <div class="gla_over" data-color="#000" data-opacity="0.7"></div>
            </div>

            <div class="gla_main_menu_content_menu gla_wht_txt text-right">
              <div class="container">
                <ul @click="flyoutmenu($event)">
                  <li v-for="(item, index) in menulist" :key="index" class="gla_parent">
                    <a :href="item.section">{{item.item}}</a>
                  </li>
                </ul>
              </div>
            </div>

            <div class="gla_default_menu">
              <ul>
                <li v-for="(item, index) in menulist" :key="index" class="gla_parent">
                  <a :href="item.section">{{item.item}}</a>
                </li>
              </ul>
            </div>
          </div>
        </nav>
      </header>

      <div
        class="gla_slider gla_image_bck gla_wht_txt gla_fixed"
        v-lazy="'https://res.cloudinary.com/dzf7mrwre/image/upload/v1670219731/DSC03130_pfpavf.png'"
        :data-image="'https://res.cloudinary.com/dzf7mrwre/image/upload/v1670219731/DSC03130_pfpavf.png'"
        data-stellar-background-ratio="0.8"
      >
        <div class="gla_over" data-color="#1e1d2d" data-opacity="0.2"></div>
        <div class="container">
          <div class="gla_slide_txt gla_slide_center_middle text-center">
            <div class="gla_flower gla_flower2">
              <div class="gla_flower2_name_l" style="margin-right: 90px !important;">
                Swapnil
                <b>
                  Save The
                  Date
                </b>
              </div>
              <div class="gla_flower2_name_r" style="margin-left: 90px !important;">
                Priyanka
                <b>
                  December 18,
                  2022
                </b>
              </div>
            </div>
            <div class="gla_slide_txt gla_slide_center_bottom text-center">
              <div class="gla_slide_midtitle_main">We're Getting Married</div>
            </div>
          </div>
        </div>
        <a class="gla_scroll_down gla_go" href="#gla_content">
          <b></b>
          Scroll
        </a>
      </div>

      <section id="gla_content" class="gla_content">

        <section class="gla_section gla_image_bck" id="wedding-hosts">
          <div class="container text-center" style="padding-bottom: 0;"> 
            <h2 style="margin-bottom:0">The Wedding Hosts</h2>
            <p style="margin-bottom:0">
              <img
                src="./images/ganesh.png"
                width="40"
                height="40"
                alt
              >
              <br>
              <b>Together with our parents, its our pleasure to cordially invite you to be the part of our big day. Please bless our new beginning with your presence.</b>
            </p>

            <div class="row text-center">
              <div v-for="(host, index) in hostlist" :key="index" class="col-md-6 gla_round_block">
                <div
                  class="gla_round_im gla_image_bck"
                  v-lazy="host.image"
                  :data-image="host.image"
                  style="width: 250px;height: 250px;display: inline-block;margin: 0 auto 20px;border-radius: 50%;position: relative;z-index: 1;"
                ></div>
                <h4>{{host.name}}</h4>
              </div>
            </div>
          </div>
        </section>

        <section class="gla_section" id="events">
          <div class="container text-center">
            <h2 style="margin-bottom:0">Main Event</h2>
          </div>
        </section>

        <section
          class="gla_section gla_image_bck gla_fixed gla_wht_txt"
          data-stellar-background-ratio="0.8"
          v-lazy="'https://images.unsplash.com/photo-1553095066-5014bc7b7f2d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80'"
          v-bind:data-image="'https://images.unsplash.com/photo-1553095066-5014bc7b7f2d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80'"
        >
          <div class="gla_over" data-color="#1e1d2d" data-opacity="0.4"></div>

          <div class="container text-center" height="700px">
            <p>
              <img
                style="margin-top:-30px"
                src="./images/animations/savethedate_wh.gif"
                height="150"
                alt
              >
            </p>
            <h2>December 18th, 2022</h2>
            <h3 class="gla_subtitle" style="margin-bottom:0">
              Gurukrupa Garden Mangal Karyalay,
              <br>Alandi Rd, Chovisawadi, Charholi Budruk, Pune.
            </h3>
            <div class="gla_countdown" data-year="2022" data-month="12" data-day="18"></div>
          </div>
        </section>

        <section class="gla_section" id="venue">
          <div class="container text-center" style="padding-bottom: 0;">
            <h2>Events & Venue Details</h2>
            <div class="row text-center">
              <div >
                <div class="col-lg-6 text-center">
                  <span class="gla_news_title">Haldi Ceremony <br> <b>16th Dec 2022</b></span>
                  <p>The haldi ceremony is usually held separately for the bride and the groom. It is a low-key event that involves the application of turmeric paste on the hands, legs and face of the bride and the groom. The groom is not allowed to see the bride after this ritual until the final wedding ceremony starts.</p>
                </div>
                <div class="col-lg-6 text-center">
                  <span class="gla_news_title">Wedding Ceremony & Reception <br> <b>18th Dec 2022</b></span>
                  <p>This is the main event in the entire wedding when the bride and the groom ties the knot. The groom comes with the barat and is greeted by the bride side followed by some rituals and of course as maximum number of guests would be attending this event. This is when the couple circle the sacred fire and are finally declared husband and wife.</p>
                </div>
              </div>
            </div>
            <div class="gla_icon_boxes row text-center">
              <div class="gla_map">
                <iframe
                  src= "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d572.8385969655732!2d73.88589588616342!3d18.659725886956746!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bc2c7d27c4cb347%3A0x49ee2ddb3a564d47!2sGurukrupa%20Garden%20Mangal%20Karyalay!5e0!3m2!1sen!2sin!4v1667192417532!5m2!1sen!2sin"
                  width="100%"
                  height="500"
                  style="padding: 50px 0;"
                ></iframe>
              </div>
              <span class="gla_news_title">Wedding Venue</span>
              <p>
                <strong>Gurukrupa Garden Mangal Karyalay</strong>
                <br>Alandi Rd, Chovisawadi, Charholi Budruk, Pune.
              </p>
              <p>
                <b>December 18th, 2022</b>
                <br>12:25 PM
                <br>
              </p>
            </div>
          </div>
        </section>

        <section class="gla_section gla_image_bck" id="glipmses">
          <div class="container text-center" style="padding-bottom:0">
            <h2 style="margin-bottom:10px">Engagement Stills</h2>
            <div class="gla_portfolio_no_padding grid">
              <div
                v-for="(image, index) in imagelist"
                :key="index"
                class="col-sm-6 gla_anim_box grid-item"
                :class="image.category"
              >
                <div class="gla_shop_item">
                  <a :href="image.image" class="lightbox">
                    <img :src="image.image" alt>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </section>

        <section>
          <div class="container text-center">
            <hr>
            <div>See you at the wedding!</div>
            <p>
              <img
                src="./images/icon-big.png"
                height="50"
                alt
              >
            </p>
          </div>
        </section>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data: function() {
    return {
      hostlist: [],
      imagelist: [],
      haldilist: [],
      menulist: {}
    };
  },
  created() {
    this.loadScripts();
  },
  mounted() {
    this.hostlist = [
      {
        image:
          "https://via.placeholder.com/200x200",
        name: "Shri Bharat Kadam"
      },
      {
        image:
          "https://res.cloudinary.com/dzf7mrwre/image/upload/v1670218744/mom_kgm47y.png",
        name: "Smt Sayali Kadam"
      }
    ];
    this.imagelist = [
      {
        image:
          "https://res.cloudinary.com/dzf7mrwre/image/upload/v1670218274/Traditional_dnqr57.png",
        category: "engagement"
      },
      {
        image:
          "https://res.cloudinary.com/dzf7mrwre/image/upload/v1670218274/mumbai_pune_zsloos.png",
        category: "engagement"
      },
      {
        image:
          "https://res.cloudinary.com/dzf7mrwre/image/upload/v1670217949/DSC03253_tfnguv.png",
        category: "engagement"
      },
      {
        image:
          "https://res.cloudinary.com/dzf7mrwre/image/upload/v1670217950/DSC03302_hu5kr3.png",
        category: "engagement"
      }
    ];
    this.menulist = [
      {
        item: "Wedding Hosts",
        section: "#wedding-hosts"
      },
      {
        item: "Main Event",
        section: "#events"
      },
      {
        item: "Venue",
        section: "#venue"
      },
      {
        item: "Engagement",
        section: "#glipmses"
      }
    ];
    this.addSmoothScroll();
  },
  methods: {
    loadScripts() {
      var bodyTag = document.getElementsByTagName("body")[0];

      var script1 = document.createElement("script");
      script1.type = "text/javascript";
      script1.src = "/static/js/ui_library.js";
      bodyTag.appendChild(script1);

      var script2 = document.createElement("script");
      script2.type = "text/javascript";
      script2.src = "/static/js/ui_script.js";
      bodyTag.appendChild(script2);
    },
    flyoutmenu(e) {
      var elems = document.querySelectorAll(".active");
      [].forEach.call(elems, function(el) {
        el.classList.remove("active");
      });
      e.target.className = "active";
    },
    addSmoothScroll() {
      $(document).ready(function() {
        $("a").on("click", function(event) {
          if (this.hash !== "") {
            event.preventDefault();
            var hash = this.hash;
            $("html, body").animate(
              {
                scrollTop: $(hash).offset().top
              },
              200,
              function() {
                window.location.hash = hash;
              }
            );
          }
        });
      });
    }
  }
};
</script>
