<template>
  <v-card elevation="2" outlined width="300px">
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
            <v-tooltip bottom>
              <template v-slot:activator="{ on, attrs }">
                <v-btn icon>
                <v-icon
                    color="grey lighten-1"
                    dark
                    v-bind="{attrs}"
                    v-on="on"
                  >
                    mdi-information
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
