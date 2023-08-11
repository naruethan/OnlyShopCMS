<template>
  <div class="container">
    <c-box w="100%" h="200" />
    <c-grid w="100%" h="200" template-columns="repeat(12, 1fr)" gap="2">
      <c-grid-item align="center" col-start="3" col-end="11" h="10">
        <c-box w="100%">
          <c-grid w="100%" h="200" template-columns="repeat(7, 1fr)" gap="5">
            <c-box w="100%" h="100%" bg="orange.300" />
            <c-box w="100%" h="100%" bg="gray.300" />
            <c-box w="100%" h="100%" bg="blue.300" />
            <c-box w="100%" h="100%" bg="orange.300" />
            <c-box w="100%" h="100%" bg="gray.300" />
            <c-box w="100%" h="100%" bg="blue.300" />
            <c-box w="100%" h="100%" bg="orange.300" />
          </c-grid>
        </c-box>
      </c-grid-item>
    </c-grid>
  </div>
</template>

<script lang="js">
import {
  CBox,
  CButton,
  CAvatarGroup,
  CAvatar,
  CAvatarBadge,
  CModal,
  CModalContent,
  CModalOverlay,
  CModalHeader,
  CModalFooter,
  CModalBody,
  CModalCloseButton,
  CIconButton,
  CFlex,
  CHeading,
  CList,
  CListIcon

} from '@chakra-ui/vue'

export default {
  name: 'IndexPage',
  components: {
    CBox,
    CButton,
    CAvatarGroup,
    CAvatar,
    CAvatarBadge,
    CModal,
    CModalContent,
    CModalOverlay,
    CModalHeader,
    CModalFooter,
    CModalBody,
    CModalCloseButton,
    CIconButton,
    CFlex,
    CHeading,
    CList,
    CListIcon
  },
  inject: ['$chakraColorMode', '$toggleColorMode'],
  data () {
    return {
      showModal: false,
      mainStyles: {
        dark: {
          bg: 'gray.700',
          color: 'whiteAlpha.900'
        },
        light: {
          bg: 'white',
          color: 'gray.900'
        }
      }
    }
  },
  computed: {
    colorMode () {
      return this.$chakraColorMode()
    },
    theme () {
      return this.$chakraTheme()
    },
    toggleColorMode () {
      return this.$toggleColorMode
    }
  },
  methods: {
    showToast () {
      this.$toast({
        title: 'Account created.',
        description: "We've created your account for you.",
        status: 'success',
        duration: 10000,
        isClosable: true
      })
    }
  }
}
</script>
