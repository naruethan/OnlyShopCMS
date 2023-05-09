<template>
  <div class="container">
    <CThemeProvider>
      <CColorModeProvider>
        <CBox font-family="body" as="main">
          <CReset />

          <c-heading as="h6" size="xs" text-align="center">
            In love with Vue & Nuxt
          </c-heading>

          <c-breadcrumb
            font-weight="medium"
            font-size="sm"
            separator=""
            align="center"
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
            </c-breadcrumb-item>
          </c-breadcrumb>

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
