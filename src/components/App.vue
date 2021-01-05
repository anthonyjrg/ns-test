<template>
    <Page>
        <FlexboxLayout flexDirection="column" backgroundColor="#3c495e">
            <ListView for="item in listOfItems" flexGrow="1"  backgroundColor="#43b883">
                <v-template>
                    <!-- Shows the list item label in the default color and style. -->
                    <Label :text="item.text" />
                </v-template>
            </ListView>

            <FlexboxLayout backgroundColor="#ffffff">
                <Button  class="btn btn-primary" flexGrow="1">
                    <FormattedString>
                        <Span class="fa" text="{{'fa-bluetooth' | fontawesome }}"></Span>
                        <Span text=" Test" fontAttributes="Bold"></Span>
                    </FormattedString>
                </Button>
            </FlexboxLayout>

        </FlexboxLayout>

    </Page>
</template>

<script lang="ts">
  export default {
    data() {
      return {
        msg: 'Hello World',
        listOfItems: [
            { text: "John"}
        ]
      }
    }
  }
</script>

<style scoped>
    ActionBar {
        background-color: #53ba82;
        color: #ffffff;
    }

    .message {
        vertical-align: center;
        text-align: center;
        font-size: 20;
        color: #333333;
    }
</style>
