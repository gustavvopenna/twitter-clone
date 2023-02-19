<template>
  <div>
    <div class="p-2 my-2 rounded-full w-min hover:bg-blue-50 dark:hover:bg-white/10" :class="defaultTransition">
      <nuxt-link to="/">
        <div class="w-8 h-8">
          <LogoTwitter />
        </div>
      </nuxt-link>
    </div>
    <SidebarLeftTab>
      <template v-slot:icon>
        <HomeIcon />
      </template>
      <template v-slot:name>
        Home
      </template>
    </SidebarLeftTab>
    
    <SidebarLeftTab>
      <template v-slot:icon>
        <HashtagIcon />
      </template>
      <template v-slot:name>
        Explore
      </template>
    </SidebarLeftTab>

    <SidebarLeftTab>
      <template v-slot:icon>
        <InboxIcon />
      </template>
      <template v-slot:name>
        Messages
      </template>
    </SidebarLeftTab>

    <SidebarLeftTab>
      <template v-slot:icon>
        <BookmarkIcon />
      </template>
      <template v-slot:name>
        Bookmarks
      </template>
    </SidebarLeftTab>

    <SidebarLeftTab>
      <template v-slot:icon>
        <DocumentTextIcon />
      </template>
      <template v-slot:name>
        List
      </template>
    </SidebarLeftTab>

    <SidebarLeftTab>
      <template v-slot:icon>
        <UserIcon />
      </template>
      <template v-slot:name>
        Profile
      </template>
    </SidebarLeftTab>

    <SidebarLeftTab>
      <template v-slot:icon>
        <EllipsisHorizontalCircleIcon />
      </template>
      <template v-slot:name>
        More
      </template>
    </SidebarLeftTab>
  </div>
</template>

<script setup>
import { HomeIcon } from '@heroicons/vue/24/solid'
import { HashtagIcon, BellIcon, InboxIcon, BookmarkIcon, DocumentTextIcon, UserIcon, EllipsisHorizontalCircleIcon } from '@heroicons/vue/24/outline'

const { defaultTransition } = useTailwind();
</script>