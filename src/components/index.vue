<template>
<div class="content column-start-center">
  <div class="overFlowNone row95 row-center">
  <div class="row110  scroll">

 <!--******************************************背景颜色样式**********************************************-->
    <div class="column5 fontStyle2 bgc1 row-flex-start">
      <div class="row10 row-center">
        背景颜色样式
      </div>
    </div>

    <div class="column50 row-start-wrap">
      <div class="box column-start-center"  v-for="(item,index) in bcgList" :class="item.type">
        <div :class="index>8?'item.type fontStyle3':'fontStyle4 item.type'">{{item.type}}</div>
      </div>
    </div>

    <!--******************************************border样式**********************************************-->
    <div class="column5 fontStyle2 bgc1 row-flex-start">
      <div class="row10 row-center">
        border样式
      </div>
    </div>

    <div class="column50 row-start-wrap">
      <div class="box column-center"  v-for="item in borderList" >

        <div class="column20 row-center">
          <div class="row80 fontStyle3 row-center":class="item.type">{{item.type}}</div>
        </div>
      </div>
    </div>


    <!--******************************************img样式**********************************************-->
    <div class="column5 fontStyle2 bgc1 row-flex-start">
      <div class="row10 row-center">
        img样式
      </div>
    </div>

    <div class="column50 row-start-wrap">
      <div class="row20 column-center box"  v-for="item in imgList" >

        <div class="column30 column-start-center fontStyle3">
          {{item.type}}
        </div>
        <div class="column70 column-center">
          <img :class="item.type" src="../img/tx.png"></img>
        </div>
      </div>
    </div>


<!--******************************************字体样式**********************************************-->
    <div class="column5 fontStyle2 bgc1 row-flex-start">
      <div class="row10 row-center">
        字体样式
      </div>
    </div>
    <div class="column10  column-center-start" v-for="item in fontList" :class="item.type" style="margin-bottom: 30px">
      <div class="column50 row-flex-start" :class="item.backColor">{{item.type}}</div>
      <div class="column50 row-flex-start" :class="item.backColor">这是一段示范文字</div>
    </div>

    <!--******************************************按钮样式**********************************************-->
    <div class="column5 fontStyle2 bgc1 row-flex-start">
      <div class="row30 row-flex-start">
        按钮组件
      </div>
    </div>
    <div class="column5 fontStyle3 row-flex-start">
      <div class="row30 row-flex-start">
        组件名：OuButton
      </div>
    </div>

    <div class="column90 row-flex-start">
      <div class="bBox column-start-center">
        <div class="column10 bgc2 fontStyle4 row-center">参数列表</div>
        <div class="column5 row-flex-start">
          <div class="row15 fontStyle3 row-center">参数名</div>
          <div class="row15 fontStyle3 row-center">参数值</div>
          <div class="row70 fontStyle3 row-center">效果</div>
        </div>

        <div class="column80  scroll">
          <div class="column20 row-center">
            <div class="row15 fontStyle3 row-center">默认</div>
            <div class="row15 fontStyle3 row-center">无</div>
            <div class="row70 fontStyle3 row-center">
              <OuButton value="默认"></OuButton>
            </div>
          </div>

          <div class="column80 row-center">
            <div class="row15 fontStyle3 row-center">size</div>
            <div class="row15 fontStyle3 column-start-center">
              <div class="column20 row-center" v-for="item in buttonList">{{item.size}}</div>

            </div>
            <div class="row70 fontStyle3 column-start-center">
              <div class="column20 row-center" v-for="it in buttonList">
              <OuButton  :size="it.size" :value="it.size"></OuButton>
              </div>
            </div>
          </div>

          <div class="column80 row-center">
            <div class="row15 fontStyle3 row-center">type</div>
            <div class="row15 fontStyle3 column-start-center">
              <div class="column20 row-center" v-for="item in buttonList">{{item.type}}</div>

            </div>
            <div class="row70 fontStyle3 column-start-center">
              <div class="column20 row-center" v-for="it in buttonList">
                <OuButton  :size="it.type" :value="it.type"></OuButton>
              </div>
            </div>
          </div>

          <div class="column5 fontStyle3 row-center">
            <div class="row80 row-center">
            以下参数为自定义参数,参数值同css
            </div>
          </div>
          <div class="column20 row-center">
          <div class="row15 fontStyle3 row-center">radius</div>
          <div class="row15 fontStyle3 row-center">示例值：20px</div>
          <div class="row70 fontStyle3 row-center">
            <OuButton value="示例20px" radius="20px"></OuButton>
          </div>
        </div>

          <div class="column20 row-center">
            <div class="row15 fontStyle3 row-center">height</div>
            <div class="row15 fontStyle3 row-center">示例值：70px</div>
            <div class="row70 fontStyle3 row-center">
              <OuButton value="示例70px" height="70px"></OuButton>
            </div>
          </div>

          <div class="column20 row-center">
            <div class="row15 fontStyle3 row-center">width</div>
            <div class="row15 fontStyle3 row-center">示例值：100px</div>
            <div class="row70 fontStyle3 row-center">
              <OuButton value="示例100px" width="100px"></OuButton>
            </div>
          </div>

          <div class="column20 row-center">
            <div class="row20 fontStyle3 row-center">backgroundColor</div>
            <div class="row15 fontStyle3 row-center">示例值：red</div>
            <div class="row65 fontStyle3 row-center">
              <OuButton value="示例red" backgroundColor="red"></OuButton>
            </div>
          </div>

          <div class="column20 row-center">
            <div class="row15 fontStyle3 row-center">fontSize</div>
            <div class="row15 fontStyle3 row-center">示例值：10px</div>
            <div class="row70 fontStyle3 row-center">
              <OuButton value="示例10px" fontSize="10px"></OuButton>
            </div>
          </div>


        </div>
      </div>
    </div>


    <!--******************************************输入框样式**********************************************-->
    <div class="column5 fontStyle2 bgc1 row-flex-start">
      <div class="row30 row-flex-start">
        输入框组件
      </div>
    </div>

    <div class="column5 fontStyle3 row-flex-start">
      <div class="row30 row-flex-start">
        组件名：OuInput
      </div>
    </div>

    <div class="column90 row-flex-start">
      <div class="bBox column-start-center">
        <div class="column10 bgc2 fontStyle4 row-center">参数列表</div>
        <div class="column5 row-flex-start">
          <div class="row15 fontStyle3 row-center">参数名</div>
          <div class="row15 fontStyle3 row-center">参数值</div>
          <div class="row70 fontStyle3 row-center">效果</div>
        </div>

        <div class="column80  scroll">
          <div class="column20 row-center">
            <div class="row15 fontStyle3 row-center">默认</div>
            <div class="row15 fontStyle3 row-center">无</div>
            <div class="row70 fontStyle3 row-center">
              <OuInput v-model="testValue"></OuInput>
            </div>
          </div>
          <div class="column60 row-center">
            <div class="row15 fontStyle3 row-center">type</div>
            <div class="row15 fontStyle3 column-center">
              <div class="column20 row-center" v-for="item in inputTypeList">{{item.type}}</div>

            </div>
            <div class="row70 fontStyle3 column-center">
              <div class="column20 row-center" v-for="it in inputTypeList">
                <OuInput  :size="it.type" :placeholder="it.type"></OuInput>
              </div>
            </div>
          </div>

          <div class="column5 fontStyle3 row-center">
            <div class="row80 row-center">
              以下参数为自定义参数,参数值同css
            </div>
          </div>
          <div class="column20 row-center">
            <div class="row15 fontStyle3 row-center">radius</div>
            <div class="row15 fontStyle3 row-center">示例值：20px</div>
            <div class="row70 fontStyle3 row-center">
              <OuInput placeholder="示例20px" radius="20px"></OuInput>
            </div>
          </div>

          <div class="column20 row-center">
            <div class="row15 fontStyle3 row-center">height</div>
            <div class="row15 fontStyle3 row-center">示例值：70px</div>
            <div class="row70 fontStyle3 row-center">
              <OuInput placeholder="示例70px" height="70px"></OuInput>
            </div>
          </div>

          <div class="column20 row-center">
            <div class="row15 fontStyle3 row-center">width</div>
            <div class="row15 fontStyle3 row-center">示例值：100px</div>
            <div class="row70 fontStyle3 row-center">
              <OuInput placeholder="示例100px" width="100px"></OuInput>
            </div>
          </div>

          <div class="column20 row-center">
            <div class="row20 fontStyle3 row-center">placeholder</div>
            <div class="row15 fontStyle3 row-center">示例值：placeholder</div>
            <div class="row65 fontStyle3 row-center">
              <OuInput  placeholder="placeholder"></OuInput>
            </div>
          </div>

          <div class="column20 row-center">
            <div class="row15 fontStyle3 row-center">fontSize</div>
            <div class="row15 fontStyle3 row-center">示例值：10px</div>
            <div class="row70 fontStyle3 row-center">
              <OuInput placeholder="示例10px" fontSize="10px"></OuInput>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!--******************************************  常用页面  **********************************************-->
    <div class="column5 fontStyle2 bgc1 row-flex-start">
      <div class="row30 row-flex-start">
        常用页面组件
      </div>
    </div>
    <div class="column5 fontStyle3 row-flex-start">
      <div class="row30 row-flex-start">
        说明：所有组件皆以height:100%/width:100%布局，请在外部限定大小
      </div>
    </div>


    <div class="column10 fontStyle3 row-flex-start">
      <div class="row5 row-flex-start">
        <OuButton value="登录" @click="changePage('login')"></OuButton>
      </div>
      <div class="row5 row-flex-start" @click="changePage('codeLogin')">
        <OuButton value="验证码登录"></OuButton>
      </div>
      <div class="row5 row-flex-start">
        <OuButton value="注册" @click="changePage('register')"></OuButton>
      </div>
      <div class="row5 row-flex-start">
        <OuButton value="经典表单" @click="changePage('classicForm')"></OuButton>
      </div>
      <div class="row5 row-flex-start">
        <OuButton value="经典表格" @click="changePage('rowTable')"></OuButton>
      </div>
      <div class="row10 row-flex-start">
        <OuButton value="管理系统经典页面" @click="changePage('manager')" width="100%"></OuButton>
      </div>
    </div>

    <div class="column90 row-center">
      <div class="row65 column-start-center">
        <div class="column85 row-center borderStyle10">
          <div class="boxStyle row-center borderStyle6">

            <div class="boxStyle1" v-show="pageShow==='login'">
              <LoginBox  ></LoginBox>
            </div>

            <div class="boxStyle1" v-show="pageShow==='codeLogin'">
              <CodeLoginBox ></CodeLoginBox>
            </div>

            <div class="boxStyle2" v-show="pageShow==='register'">
              <RegisterBox ></RegisterBox>
            </div>

            <div class="boxStyle4" v-show="pageShow==='rowTable'">
              <RowTable ></RowTable>
            </div>

            <div class="boxStyle7" v-show="pageShow==='classicForm'">
              <ClassicForm ></ClassicForm>
            </div>



            <router-view v-show="pageShow==='manager'"></router-view>

          </div>
        </div>
        <div class="column10 row-center">
          <div class="row15 bgc0 borderStyle"></div>
        </div>
        <div class="column5  row-center ">
          <div class="row50 bgc0"></div>
        </div>
      </div>

    </div>


    <!--******************************************  移动端常用布局  **********************************************-->

    <div class="column5 fontStyle2 bgc1 row-flex-start">
      <div class="row30 row-flex-start ">
        移动端常用布局
      </div>
    </div>
    <div class="column10 fontStyle3 row-flex-start">
      <div class="row5 row-flex-start">
        <OuButton value="布局1" @click="changeMPage('login')"></OuButton>
      </div>
      <div class="row5 row-flex-start" @click="changeMPage('codeLogin')">
        <OuButton value="布局2"></OuButton>
      </div>
      <div class="row5 row-flex-start">
        <OuButton value="布局3" @click="changeMPage('register')"></OuButton>
      </div>
      <div class="row5 row-flex-start">
        <OuButton value="布局4" @click="changeMPage('classicForm')"></OuButton>
      </div>
 

    </div>

    <div class="column75 row-center">
      <div class="row18 column-start-center">
        <div class="column10 modelH column-center">
          <div class="column10 row-center">
            <div class="row15 bgc0 borderStyle"></div>
          </div>
        </div>
        <div class="column70  row-center">
          <div class="row5 modelCL"></div>
          <div class="row90 "></div>
          <div class="row5 modelCR"></div>

        </div>
        <div class="column10 modelB column-center">
          <div class="column65 row-center">
            <div class="row15 modelBB borderStyle"></div>
          </div>
        </div>
      </div>
    </div>



    <!--******************************************  布局**********************************************-->
    <div class="column5 fontStyle2 bgc1 row-flex-start">
      <div class="row10 row-center">
        布局
      </div>
    </div>
    <div class="column5 fontStyle3 row-flex-start">
      <div class="row30 row-flex-start">
        说明：以下所有的示范容器代表长宽各为100%的浏览器窗口,且所有布局只适用于flex
      </div>
    </div>
    <!--******************************************  .column5~.column95**********************************************-->
    <div class="column5 fontStyle3 row-flex-start">
      <div class="row15 row-center">
        .column5~.column95
      </div>
    </div>
    <div class="column50 row-start-wrap">
      <div class="box column-start-center"  v-for="item in columnList">
        <div class="bgc1 fontStyle4" :class="item.type">{{item.type}}</div>
      </div>
    </div>
    <!--******************************************  .row5~.row95**********************************************-->
    <div class="column5 fontStyle3 row-flex-start">
      <div class="row15 row-center">
        .row5~.row95
      </div>
    </div>
    <div class="column50 row-start-wrap">
      <div class="box row-flex-start"  v-for="item in rowList">
        <div class="bgc1 fontStyle4" :class="item.type">{{item.type}}</div>
      </div>
    </div>
    <!--****************************************** 纵向布局(column)**********************************************-->
    <div class="column5 fontStyle3 row-flex-start">
      <div class="row15 row-center">
        纵向布局(column)
      </div>
    </div>
    <div class="column30 row-start-wrap">
      <div class="row10 column-center" v-for="item in columnLayout" style="margin-right: 10px">
        <div class="column20 row-flex-start fontStyle3">{{item.type}}</div>
        <div class="cBox" :class="item.type" >
          <div class="columnLine bgc1 fontStyle4"></div>
          <div class="columnLine bgc2"></div>
          <div class="columnLine bgc3"></div>
        </div>
      </div>
    </div>

    <!--****************************************** 横向布局(row)**********************************************-->
    <div class="column5 fontStyle3 row-flex-start">
      <div class="row15 row-center">
        横向布局(row)
      </div>
    </div>
    <div class="column30 row-start-wrap" style="margin-bottom: 20px">
      <div class="row10 column-center" v-for="item in rowLayout" style="margin-right: 10px">
        <div class="column20 row-flex-start fontStyle3">{{item.type}}</div>
        <div class="cBox" :class="item.type" >
          <div class="rowLine bgc1 fontStyle4"></div>
          <div class="rowLine bgc2"></div>
          <div class="rowLine bgc3"></div>
        </div>
      </div>
    </div>




  </div>
  </div>

</div>
</template>

<script>
    export default {
      watch:{
        testValue(curVal,oldVal){
          console.log(curVal);
        },
      },
      data(){
        return{
          columnList:[
            {type:'column10'
            },
            {type:'column15'},
            {type:'column20'},
            {type:'column25'},
            {type:'column30'},
            {type:'column35'},
            {type:'column40'},
            {type:'column45'},
            {type:'column50'},
            {type:'column55'},
            {type:'column60'},
            {type:'column65'},
            {type:'column70'},
            {type:'column75'},
            {type:'column80'},
            {type:'column85'},
            {type:'column90'},
            {type:'column95'}
          ],
          rowList:[
            {type:'row10'},
            {type:'row15'},
            {type:'row20'},
            {type:'row25'},
            {type:'row30'},
            {type:'row35'},
            {type:'row40'},
            {type:'row45'},
            {type:'row50'},
            {type:'row55'},
            {type:'row60'},
            {type:'row65'},
            {type:'row70'},
            {type:'row75'},
            {type:'row80'},
            {type:'row85'},
            {type:'row90'},
            {type:'row95'}
          ],
          columnLayout:[
            {type:'column-center'},
            {type:'column-start-start'},
            {type:'column-start-center'},
            {type:'column-center-start'},
            {type:'column-end'},
            {type:'column-end-start'},
            {type:'column-space-around'},
            {type:'column-space-start'},
          ],
          rowLayout:[
            {type:'row-center'},
            {type:'row-center-start'},
            {type:'row-space-around'},
            {type:'row-flex-start'},
            {type:'row-start-wrap'},
            {type:'row-flex-end'},
            {type:'row-start-end'},
            {type:'row-space-between'},
          ],
          fontList:[
            {type:'fontStyle1',
            backColor:''
            },
            {type:'fontStyle2',
              backColor:'bgc2'
            },
            {type:'fontStyle3',
              backColor:''
            },
            {type:'fontStyle4',
              backColor:'bgc2'
            },
          ],
          buttonList:[
            {
              type:'warm',
              size:'m',
            },
            {
              type:'info',
              size:'l',
            },
            {
              type:'danger',
              size:'xl',
            },
            {
              type:'success',
              size:'xxl',
            },
          ],
          zdyButtonList:[
            {
              type:'radius',
              description:'示例值：20px',
              value:'20px'
            },
            {
              type:'height',
              description:'示例值：100px',
              value:'100px'
            },
            {
              type:'value',
              description:'示例值：100px',
              value:'100px'
            },
            {
              type:'backgroundColor',
              description:'示例值：red',
              value:'red'
            },
            {
              type:'fontSize',
              description:'示例值：20px',
              value:'20px'
            }
          ],
          inputList:[
            {
              type:'noBorder',
              size:'m',
            },
            {
              type:'line',
              size:'l',
            },
            {
              size:'xl',
            },
            {
              size:'xxl',
            },
          ],
          inputTypeList:[
            {
              type:'noBorder',
            },
            {
              type:'line',
            }
          ],
          testValue:'',
          bcgList:[
            {
              type:'bgc0'
            },
            {
              type:'bgc1'
            },
            {
              type:'bgc2'
            },
            {
              type:'bgc3'
            },
            {
              type:'bgc4'
            },
            {
              type:'bgc5'
            },
            {
              type:'bgc6'
            },
            {
              type:'bgc7'
            },
            {
              type:'bgc8'
            },
            {
              type:'bgc9'
            },
            {
              type:'bgc10'
            },
            {
              type:'bgc11'
            },
            {
              type:'bgc12'
            },

          ],
          borderList:[
            {
              type:'borderStyle'
            },
            {
              type:'borderStyle1'
            },
            {
              type:'borderStyle2'
            },
            {
              type:'borderStyle3'
            },
            {
              type:'borderStyle4'
            },
            {
              type:'borderStyle5'
            }
            ,
            {
              type:'borderStyle6'
            },
            {
              type:'borderStyle7'
            },
            {
              type:'borderStyle8'
            }
            ,
            {
              type:'borderStyle9'
            }

          ],
          imgList:[
            {
              type:'imgStyle'
            },
            {
              type:'imgStyle1'
            },
            {
              type:'imgStyle2'
            },
            {
              type:'imgStyle3'
            },
            {
              type:'imgStyle4'
            },
            {
              type:'imgStyle5'
            }
            ,
            {
              type:'imgStyle6'
            },
            {
              type:'imgStyle7'
            },
            {
              type:'imgStyle8'
            }
            ,
            {
              type:'imgStyle9'
            }
            ,        {
              type:'imgStyle10'
            },
            {
              type:'imgStyle11'
            },
            {
              type:'imgStyle12'
            },
            {
              type:'imgStyle13'
            },
            {
              type:'imgStyle14'
            },
            {
              type:'imgStyle15'
            }
            ,
     /*       {
              type:'imgStyle16'
            },
            {
              type:'imgStyle17'
            },
            {
              type:'imgStyle18'
            }
            ,
            {
              type:'imgStyle19'
            }*/
          ],
          pageShow:'login',
          phonePageShow:'layout1'
        }
      },
        name: "",
      methods:{
          changePage(s){
            this.pageShow=s
            if(s === 'manager') {
              this.$router.push({ path: 'home' })
            }
          },
          changeMPage(s){

          },
          httpTest() {
            this.$http({
              url: this.$http.adornUrl(''),
              method: 'get',
              params: {}
            }).then(({data}) => {
              console.log(data)
            })
        }
      }
    }
</script>

<style scoped>
  .modelH{
    border-top-left-radius: 25px;
    border-top-right-radius: 25px;
  /*box-shadow: h-shadow v-shadow blur spread color inset; 水平阴影的位置,垂直阴影的位置,模糊距离,阴影的尺寸,阴影的颜色,inset/outset*/
    box-shadow: 0px 5px 10px 5px #e2e2e2 inset;
  }
  .modelB{
    border-bottom-left-radius: 25px;
    border-bottom-right-radius: 25px;
    /*box-shadow: h-shadow v-shadow blur spread color inset; 水平阴影的位置,垂直阴影的位置,模糊距离,阴影的尺寸,阴影的颜色,inset/outset*/
    box-shadow: 0px -5px 10px 5px #e2e2e2 inset;
  }
  .modelCR{
    box-shadow: -5px 0px 5px 3px #e6e6e6 inset;
  }
  .modelCL{
    box-shadow: 5px 0px 5px 3px #e6e6e6 inset;
  }
  .modelBB{
    border-radius: 50%;
    box-shadow: 0px 0px 3px 3px #d9d9d9 inset;
  }
.box{
  width: 10%;
  height: 40%;
  border-radius: 5px;
  border: 2px solid gray;
  margin-right:10px;
}
.cBox{
  width: 90%;
  height: 100%;
  border-radius: 5px;
  border: 2px solid gray;
  margin-right:10px;
}
.bBox{
  width: 45%;
  height: 90%;
  border-radius: 25px;
  border: 1px solid gray;
  overflow: auto;
}
  .scroll{
    overflow:auto;
  }
  .overFlowNone{
    overflow: hidden;
  }
  .columnLine{
    height: 20%;
    width: 80%;
  }
.rowLine{
  height: 50%;
  width: 20%;
}
</style>
