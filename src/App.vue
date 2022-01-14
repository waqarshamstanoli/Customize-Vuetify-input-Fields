<template>
  <v-app>
    <v-main>
    <v-card class="mt-15 mx-auto" width="200" height="200">
    <v-card-text>
<v-text-field outlined dense label="Enter Text"></v-text-field>  
<v-select outlined dense label="Select Item"></v-select>
   <v-menu
            v-model="menu"
            :close-on-content-click="false"
            :nudge-right="40"
            transition="scale-transition"
            offset-y
          >
            <template v-slot:activator="{ on, attrs }">
              <v-text-field 
                v-model="date"
                append-icon="mdi-calendar"
                readonly
                dense
                outlined
                v-bind="attrs"
                label="Date"
                v-on="on"
                max-width="20%"
                class="date elevation-0"
                background-color="transparent"
              ></v-text-field>
            </template>
            <v-date-picker
              v-model="date"
              @input="menu = false"
              color="#950014"
            ></v-date-picker>
          </v-menu>
</v-card-text>
</v-card>    
    </v-main>
  </v-app>
</template>

<style lang="scss">
.v-text-field--outlined fieldset {
    color: #950014 !important;
}
.v-input input {
    max-height: 32px;
    color: #950014 !important;
}
.date.v-input input {
    max-height: 32px;
    color: #950014 !important;
  
}
 .v-select__selection,
.v-select__selection--comma,
.v-select.v-text-field input {
  color: #950014 !important;
}
.v-text-field--outlined.v-input--dense .v-label {
    color: #950014 !important;
}

.v-icon.notranslate.mdi.mdi-calendar.theme--light{
  color: #950014 !important;
}
.v-icon.notranslate.mdi.mdi-menu-down.theme--light{
  color: #950014 !important;
}


</style>

