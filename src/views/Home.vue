<template>
  <div>
    <div>
      <b-navbar type="dark" variant="dark">
        <b-navbar-nav>
          <b-nav-item href="#" v-b-toggle.sidebar-no-header>Home</b-nav-item>
        </b-navbar-nav>
      </b-navbar>
    </div>
    <b-sidebar
      id="sidebar-no-header"
      aria-labelledby="sidebar-no-header-title"
      title="Menu"
      shadow
    >
      <template v-slot:default="{ hide }">
        <div class="p-3">
          <h4 id="sidebar-no-header-title">Message from your teacher</h4>
          <p>Cras mattis consectetur purus sit amet fermentum.</p>
          <nav class="mb-3">
            <b-nav vertical>
              <b-nav-item active @click="hide">Active</b-nav-item>
              <b-nav-item href="#link-1" @click="hide">Link</b-nav-item>
              <b-nav-item href="#link-2" @click="hide">Another Link</b-nav-item>
            </b-nav>
          </nav>
          <b-button variant="primary" block @click="hide">
            Close Sidebar
          </b-button>
        </div>
      </template>
    </b-sidebar>
  </div>
</template>
