<template>
  <sidebar />
  <platform-header
    class="inverted bg-white platform-loaded"
    title-text="Credit limit"
    app-icon="fa fa-gamepad"
    data-platform-header-ready
  >
    <platform-header-container>
      <label for="cm-sidenav-toggle">
        <svg
          width="24px"
          height="24px"
          viewBox="0 0 24 24"
          version="1.1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
        >
          <path
            d="M18,18 L6,18 C5.447,18 5,17.552 5,17 C5,16.448 5.447,16 6,16 L18,16 C18.553,16 19,16.448 19,17 C19,17.552 18.553,18 18,18 M18,13 L6,13 C5.447,13 5,12.552 5,12 C5,11.448 5.447,11 6,11 L18,11 C18.553,11 19,11.448 19,12 C19,12.552 18.553,13 18,13 M18,8 L6,8 C5.447,8 5,7.552 5,7 C5,6.448 5.447,6 6,6 L18,6 C18.553,6 19,6.448 19,7 C19,7.552 18.553,8 18,8"
          ></path>
        </svg>
      </label>
      <label class="platform-no-menu" for="platform-header-no-menu">
        <a
          class="logo"
          href="https://www.cm.com/en-gb/app/dashboard"
          target="_self"
          title="CM.com"
        >
          <img src="https://www.cm.com/cdn/cm/cm.svg" alt="CM.com" />
          <div class="title">Credit limit</div>
        </a>
      </label>

      <platform-header-menu>
        <input
          type="radio"
          name="platform-header-menu-toggle"
          id="platform-header-no-menu"
          checked=""
        />
        <platform-menu-component>
          <div class="header-nav-left">
            <ul>
              <li class="nav-item">
                <a href="#"
                  ><span
                    class="cm-icon cm-icon-help-open"
                    aria-hidden="true"
                  ></span
                ></a>
              </li>
              <li class="nav-item">
                <a href="#"
                  ><span class="cm-icon cm-icon-apps" aria-hidden="true"></span
                ></a>
              </li>
              <li class="nav-item nav-icon">
                <span
                  class="cm-icon cm-icon-user-fill f-37"
                  aria-hidden="true"
                ></span>
              </li>
              <li class="nav-item nav-item__name">
                <span class="cm-name">Justine</span>
                <span class="cm-account">Account A</span>
              </li>
              <li class="nav-item">
                <span
                  class="cm-icon cm-icon-arrow-right"
                  aria-hidden="true"
                ></span>
              </li>
            </ul>
          </div>
        </platform-menu-component>
      </platform-header-menu>
    </platform-header-container>
  </platform-header>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Sidebar from "./Sidebar.vue";

export default defineComponent({
  name: "Header",
  components: {
    Sidebar,
  },
});
</script>

<style lang="scss" scoped>
.header-nav-left {
  position: relative;
  z-index: 10;
}

.header-nav-left > ul {
  display: inline-flex;
  align-items: center;
}

.header-nav-left > ul > li > a {
  color: inherit;
  font-size: 14px;
}

.header-nav-left .nav-item.nav-item__name {
  display: inline-flex;
  flex-direction: column;
  align-items: flex-start;
  line-height: normal;
  margin-bottom: 10px;
}

.header-nav-left .nav-item.nav-icon .cm-icon {
  font-size: 36px;
}

.header-nav-left .nav-item {
  margin-right: 14px;
}

.header-nav-left .nav-item:last-child {
  margin-right: 0;
}

.header-nav-left .nav-item.nav-item__name .cm-name {
  font-weight: 600;
  font-size: 14px;
}

.header-nav-left .nav-item.nav-item__name .cm-account {
  font-size: 12px;
}
</style>
