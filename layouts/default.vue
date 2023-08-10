<template>
  <div class="container">
    <CThemeProvider>
      <CColorModeProvider>
        <CBox font-family="body" p="4" as="main">
          <CReset />

          <c-grid w="100%" template-columns="repeat(12, 1fr)" gap="2">
            <c-grid-item col-span="2" h="10"
              ><c-text fontSize="xl" align="left"
                >Shabu Kru.Watree Shop</c-text
              ></c-grid-item
            >

            <c-grid-item
              align="center"
              col-start="4"
              col-end="10"
              h="10"
              bg="red.300"
            >
              <c-breadcrumb-item>
                <c-breadcrumb-link as="nuxt-link" to="/">
                  <c-button variant-color="green"
                    >Home</c-button
                  ></c-breadcrumb-link
                >
              </c-breadcrumb-item>

              <c-breadcrumb-item>
                <c-breadcrumb-link as="nuxt-link" to="/Test2"
                  ><c-button variant-color="yellow"
                    >Order</c-button
                  ></c-breadcrumb-link
                >
              </c-breadcrumb-item>
              <c-breadcrumb-item>
                <c-breadcrumb-link as="nuxt-link" to="/Test3"
                  ><c-button variant-color="blue"
                    >Check out</c-button
                  ></c-breadcrumb-link
                >
              </c-breadcrumb-item></c-grid-item
            >
            <c-box w="100%" h="10" bg="orange.300" />
          </c-grid>
          <Nuxt />
        </CBox>
      </CColorModeProvider>
    </CThemeProvider>
  </div>
</template>
<script>
import {
  CThemeProvider,
  CColorModeProvider,
  CReset,
  CBox,
  CButton,
  CBreadcrumb,
  CHeading,
  CMenu,
  CGrid,
  CGridItem,
  CFlex,
} from "@chakra-ui/vue";

export default {
  name: "DefaultLayout",
  components: {
    CThemeProvider,
    CColorModeProvider,
    CReset,
    CBox,
    CButton,
    CBreadcrumb,
    CHeading,
    CGridItem,
    CGrid,
    CFlex,
  },
};
</script>
