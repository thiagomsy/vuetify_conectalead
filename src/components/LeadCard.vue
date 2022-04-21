<template>
  <v-card elevation="2" outlined height="128px" width="300px" style="position: relative">
    <v-card-text>
      <v-list>
        <v-list-item>
          <v-list-item-avatar :color="icon_color+'4d'">
            <v-icon
              :color="icon_color"
            >
              {{icon_name}}
            </v-icon>
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title class="font-weight-bold" style="color: #2c3e50; font-size: 32px" v-text="value"></v-list-item-title>

            <v-list-item-subtitle style="color: #2c3e50; font-size: 16px" v-text="name"></v-list-item-subtitle>
          </v-list-item-content>

          <v-list-item-action>
            <v-tooltip top>
              <template v-slot:activator="{ on, attrs }">
                <v-btn icon color="#608289" class="tooltip-icon">
                  <v-icon
                    v-bind="{attrs}"
                    v-on="on"
                  >
                    mdi-information-outline
                  </v-icon>
                </v-btn>
              </template>
              <span>{{subtitle}}</span>
            </v-tooltip>
          </v-list-item-action>
        </v-list-item>
      </v-list>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  props: ["name", "value", "subtitle", "icon_name", "icon_color"],
};
</script>

<style scoped>
  .tooltip-icon{
    position: absolute;
    right: -16px;
    top: -24px;
  }
</style>