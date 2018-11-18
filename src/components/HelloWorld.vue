<template>
  <v-container ref="HelloWorld_container">
    <div class="d_container" ref="d_container" v-if="!show_output">
      <v-expansion-panel focusable>
        <v-expansion-panel-content>
          <div slot="header">7.反空汙公投</div>
          <v-card>
            <v-card-text>你是否同意以「平均每年至少降低1%」之方式逐年降低火力發電廠發電量？</v-card-text>
            <v-card-actions>
              <v-radio-group v-model="p7">
                <v-radio :value="true" color="success">
                  <div slot="label"><strong class="success--text">同意</strong></div>
                </v-radio>
                <v-radio :value="false" color="error">
                  <div slot="label"><strong class="error--text">不同意</strong></div>
                </v-radio>
              </v-radio-group>
            </v-card-actions>
          </v-card>
        </v-expansion-panel-content>
        <v-expansion-panel-content>
          <div slot="header">8.反深澳電廠</div>
          <v-card>
            <v-card-text>您是否同意確立「停止新建、擴建任何燃煤發電廠或發電機組（包括深澳電廠擴建）」之能源政策？</v-card-text>
            <v-card-actions>
              <v-radio-group v-model="p8">
                <v-radio :value="true" color="success">
                  <div slot="label"><strong class="success--text">同意</strong></div>
                </v-radio>
                <v-radio :value="false" color="error">
                  <div slot="label"><strong class="error--text">不同意</strong></div>
                </v-radio>
              </v-radio-group>
            </v-card-actions>
          </v-card>
        </v-expansion-panel-content>
        <v-expansion-panel-content>
          <div slot="header">9.反核食進口</div>
          <v-card>
            <v-card-text>你是否同意政府維持禁止開放日本福島311核災相關地區，包括福島與周遭4縣市（茨城、櫪木、群馬、千葉）等地區農產品及食品進口？</v-card-text>
            <v-card-actions>
              <v-radio-group v-model="p9">
                <v-radio :value="true" color="success">
                  <div slot="label"><strong class="success--text">同意</strong></div>
                </v-radio>
                <v-radio :value="false" color="error">
                  <div slot="label"><strong class="error--text">不同意</strong></div>
                </v-radio>
              </v-radio-group>
            </v-card-actions>
          </v-card>
        </v-expansion-panel-content>
        <v-expansion-panel-content>
          <div slot="header">10. 婚姻限一男一女</div>
          <v-card>
            <v-card-text>你是否同意民法婚姻規定應限定在一男一女的結合？</v-card-text>
            <v-card-actions>
              <v-radio-group v-model="p10">
                <v-radio :value="true" color="success">
                  <div slot="label"><strong class="success--text">同意</strong></div>
                </v-radio>
                <v-radio :value="false" color="error">
                  <div slot="label"><strong class="error--text">不同意</strong></div>
                </v-radio>
              </v-radio-group>
            </v-card-actions>
          </v-card>
        </v-expansion-panel-content>
        <v-expansion-panel-content>
          <div slot="header">11. 高中前不教同志教育</div>
          <v-card>
            <v-card-text>你是否同意在國民教育階段內（國中及國小），教育部及各級學校不應對學生實施性別平等教育法施行細則所定之同志教育？</v-card-text>
            <v-card-actions>
              <v-radio-group v-model="p11">
                <v-radio :value="true" color="success">
                  <div slot="label"><strong class="success--text">同意</strong></div>
                </v-radio>
                <v-radio :value="false" color="error">
                  <div slot="label"><strong class="error--text">不同意</strong></div>
                </v-radio>
              </v-radio-group>
            </v-card-actions>
          </v-card>
        </v-expansion-panel-content>
        <v-expansion-panel-content>
          <div slot="header">12.同志生活權益用專法</div>
          <v-card>
            <v-card-text>你是否同意以民法婚姻規定以外之其他形式來保障同性別二人經營永久共同生活的權益？</v-card-text>
            <v-card-actions>
              <v-radio-group v-model="p12">
                <v-radio :value="true" color="success">
                  <div slot="label"><strong class="success--text">同意</strong></div>
                </v-radio>
                <v-radio :value="false" color="error">
                  <div slot="label"><strong class="error--text">不同意</strong></div>
                </v-radio>
              </v-radio-group>
            </v-card-actions>
          </v-card>
        </v-expansion-panel-content>
        <v-expansion-panel-content>
          <div slot="header">13. 2020東京奧運正名</div>
          <v-card>
            <v-card-text>你是否同意，以「台灣」（Taiwan）為全名申請參加所有國際運動賽事及2020年東京奧運？</v-card-text>
            <v-card-actions>
              <v-radio-group v-model="p13">
                <v-radio :value="true" color="success">
                  <div slot="label"><strong class="success--text">同意</strong></div>
                </v-radio>
                <v-radio :value="false" color="error">
                  <div slot="label"><strong class="error--text">不同意</strong></div>
                </v-radio>
              </v-radio-group>
            </v-card-actions>
          </v-card>
        </v-expansion-panel-content>
        <v-expansion-panel-content>
          <div slot="header">14. 民法保障同志權益</div>
          <v-card>
            <v-card-text>您是否同意，以民法婚姻章保障同性別二人建立婚姻關係？</v-card-text>
            <v-card-actions>
              <v-radio-group v-model="p14">
                <v-radio :value="true" color="success">
                  <div slot="label"><strong class="success--text">同意</strong></div>
                </v-radio>
                <v-radio :value="false" color="error">
                  <div slot="label"><strong class="error--text">不同意</strong></div>
                </v-radio>
              </v-radio-group>
            </v-card-actions>
          </v-card>
        </v-expansion-panel-content>
        <v-expansion-panel-content>
          <div slot="header">15. 國中小性別平等教育</div>
          <v-card>
            <v-card-text>您是否同意，以「性別平等教育法」明定在國民教育各階段內實施性別平等教育，且內容應涵蓋情感教育、性教育、同志教育等課程？</v-card-text>
            <v-card-actions>
              <v-radio-group v-model="p15">
                <v-radio :value="true" color="success">
                  <div slot="label"><strong class="success--text">同意</strong></div>
                </v-radio>
                <v-radio :value="false" color="error">
                  <div slot="label"><strong class="error--text">不同意</strong></div>
                </v-radio>
              </v-radio-group>
            </v-card-actions>
          </v-card>
        </v-expansion-panel-content>
        <v-expansion-panel-content>
          <div slot="header">16. 廢除「非核家園」條文</div>
          <v-card>
            <v-card-text>您是否同意：廢除電業法第95條第1項，即廢除『核能發電設備應於中華民國一百十四年以前，全部停止運轉』之條文？</v-card-text>
            <v-card-actions>
              <v-radio-group v-model="p16">
                <v-radio :value="true" color="success">
                  <div slot="label"><strong class="success--text">同意</strong></div>
                </v-radio>
                <v-radio :value="false" color="error">
                  <div slot="label"><strong class="error--text">不同意</strong></div>
                </v-radio>
              </v-radio-group>
            </v-card-actions>
          </v-card>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </div>
    <Output v-if="show_output"
      :p7="p7"
      :p8="p8"
      :p9="p9"
      :p10="p10"
      :p11="p11"
      :p12="p12"
      :p13="p13"
      :p14="p14"
      :p15="p15"
      :p16="p16"
    ></Output>
    <v-btn v-if="!show_output" color="success" @click="next">下一步</v-btn>
    <v-btn v-if="show_output" @click="show_output = false">上一步</v-btn>
  </v-container>
</template>

<script>
  import domtoimage from 'dom-to-image';
  import Output from './Output.vue';

  export default {
    components: {Output},
    data: () => ({
      p7: false,
      p8: false,
      p9: false,
      p10: false,
      p11: false,
      p12: false,
      p13: false,
      p14: false,
      p15: false,
      p16: false,
      show_output: false
    }),
    methods: {
      next(){
        this.show_output = true;

        // let node = this.$refs.d_container;
        
        // domtoimage.toPng(node)
        // .then((dataUrl)=> {
        //     var img = new Image();
        //     img.src = dataUrl;
        //     this.$refs.myoutput.appendChild(img);
        // })
        // .catch(function (error) {
        //     console.error('oops, something went wrong!', error);
        // });
      }
    },
    
  }
</script>

<style>

</style>
