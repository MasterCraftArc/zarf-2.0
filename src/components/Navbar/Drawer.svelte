<script>
  import { onMount, afterUpdate } from 'svelte';
  import { Drawer, Button, CloseButton, Sidebar, SidebarBrand, SidebarCta, SidebarDropdownItem, SidebarDropdownWrapper, SidebarGroup, SidebarItem, SidebarWrapper } from 'flowbite-svelte';
  import { sineIn } from 'svelte/easing';
  import hamburger from '../../assets/png/hamburger_menu-removebg-preview.png';

  let hidden2 = true;
  let transitionParams = {
    x: -320,
    duration: 200,
    easing: sineIn
  };

  let sidebarBackgroundColor = '#0D133D';

  onMount(() => {
    hidden2 = false;
  });

  afterUpdate(() => {
    hidden2 = true;
  });
</script>

<div class="text-center">
  <Button on:click={() => (hidden2 = false)} id="something" class="button-no-background" style="background-color: transparent;">
    <img src="{hamburger}" alt="">
  </Button>
</div>

<Drawer transitionType="fly" {transitionParams} bind:hidden={hidden2} id='sidebar2' style="background-color: {sidebarBackgroundColor}">
  <div class='flex items-center'>
    <h5 id="drawer-navigation-label-3" class="text-base font-semibold text-white uppercase dark:text-gray-400">Menu</h5>
    <CloseButton on:click={() => (hidden2 = true)} class='mb-4 dark:text-white' style="color: white;">
      <style>
        .close-button:hover {
          background-color: inherit;
        }
      </style>
    </CloseButton>
  </div>
  <Sidebar>
    <SidebarWrapper divClass='overflow-y-auto py-4 px-3 rounded' style="background-color: {sidebarBackgroundColor};">
      <style>
        .sidebar-item:hover {
          background-color: inherit;
        }
      </style>
      <SidebarGroup>
        <SidebarItem label="Product" class="text-white sidebar-item"></SidebarItem>
        <SidebarItem label="Examples" class="text-white sidebar-item"></SidebarItem>
        <SidebarItem label="Docs" class="text-white sidebar-item"></SidebarItem>
      </SidebarGroup>
    </SidebarWrapper>
  </Sidebar>
</Drawer>

<style>
  img {
    height: 30px;
  }
</style>
