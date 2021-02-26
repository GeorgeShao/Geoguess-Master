<template>
  <v-card color="#E1F5FE">
    <v-card-title>
      <span>Input your room size.</span>
    </v-card-title>
    <v-card-text>
      <v-container>
        <v-row>
          <v-col cols="4">
            <v-select 
              v-model="state.roomSize"
              :items="state.roomSizeItems"></v-select>
          </v-col>        
        </v-row>
      </v-container>
    </v-card-text>
    <v-card-actions>
      <div class="flex-grow-1"></div>
      <v-btn
        dark
        depressed
        color="#43B581"
        @click="setRoomSize">NEXT</v-btn>
      <v-btn
        dark
        depressed
        color="#FF5252"
        @click="cancel">CANCEL</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script lang="ts">
import { defineComponent, reactive, } from '@vue/composition-api'

declare interface RoomSizeItem {
  text: string;
  value: number;
}

export default defineComponent({
  
  setup(props, context) {

    const state = reactive<{
      roomSize: number;
      roomSizeItems: RoomSizeItem[],
    }>({
      roomSize: 2,
      roomSizeItems: [
        {
          text: '2',
          value: 2,
        },
        {
          text: '3',
          value: 3,
        },
        {
          text: '4',
          value: 4,
        },
        {
          text: '5',
          value: 5,
        },
        {
          text: '6',
          value: 6,
        },
        {
          text: '7',
          value: 7,
        },
        {
          text: '8',
          value: 8,
        },
        {
          text: '9',
          value: 9,
        },
        {
          text: '10',
          value: 10,
        },
        {
          text: '11',
          value: 11,
        },
        {
          text: '12',
          value: 12,
        },
        {
          text: '13',
          value: 13,
        },
        {
          text: '14',
          value: 14,
        },
        {
          text: '15',
          value: 15,
        },
        {
          text: '16',
          value: 16,
        },
        {
          text: '17',
          value: 17,
        },
        {
          text: '18',
          value: 18,
        },
        {
          text: '19',
          value: 19,
        },
        {
          text: '20',
          value: 20,
        },
        {
          text: '21',
          value: 21,
        },
        {
          text: '22',
          value: 22,
        },
        {
          text: '23',
          value: 23,
        },
        {
          text: '24',
          value: 24,
        },
        {
          text: '25',
          value: 25,
        },
        {
          text: '30',
          value: 30,
        },
        {
          text: '31',
          value: 31,
        },
        {
          text: '32',
          value: 32,
        },
        {
          text: '33',
          value: 33,
        },
        {
          text: '34',
          value: 34,
        },
        {
          text: '35',
          value: 35,
        },
        {
          text: '36',
          value: 36,
        },
        {
          text: '37',
          value: 37,
        },
        {
          text: '38',
          value: 38,
        },
        {
          text: '39',
          value: 39,
        },
        {
          text: '40',
          value: 40,
        },
        {
          text: '41',
          value: 41,
        },
        {
          text: '42',
          value: 42,
        },
        {
          text: '43',
          value: 43,
        },
        {
          text: '44',
          value: 44,
        },
        {
          text: '45',
          value: 45,
        },
      ]
    })

    function setRoomSize(): void {
      context.emit('setRoomSize', state.roomSize)
    }

    function cancel(): void {
      context.emit('cancel')
    }

    return {
      state,
      setRoomSize,
      cancel,
    }
  }
})
</script>

<style scoped>

</style>
