<template>
  <div class="container">
    <ThemeProvider>
      <ColorModeProvider v-slot="{ colorMode }">
        <Box
          font-family="body"
          as="main"
          :bg="colorMode === 'light' ? 'white' : 'gray.800'"
          :color="colorMode === 'light' ? 'black' : 'whiteAlpha.900'"
        >
          <Navbar />
          <Nuxt />
        </Box>
      </ColorModeProvider>
    </ThemeProvider>
  </div>
</template>
<script>
import { ThemeProvider, ColorModeProvider, Box } from 'chakra-ui-core'
import Navbar from '../components/Navbar'

export default {
  name: 'HomeLayout',
  components: {
    ThemeProvider,
    ColorModeProvider,
    Box,
    Navbar
  }
}
</script>
