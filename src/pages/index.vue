<template>
  <div>
    <el-row :gutter="0" type="flex" justify="center" align="top">
      <el-col :span="8">
        <config-title
          :size="28"
          :weight="false"
          :italic="false"
          :underline="false"
          title-style="title-null"
          color="rgba(252, 79, 66, 1)"
          vertical="center"
          inner-text="9999"
          :url_type="0"
          :page_new_window="false"
          :href_new_window="false"
        ></config-title>
        <config-title
          :size="23"
          :weight="false"
          :italic="false"
          :underline="false"
          title-style="title-null"
          color="rgba(93, 129, 249, 1)"
          vertical="center"
          inner-text="日活"
          :url_type="0"
          :page_new_window="false"
          :href_new_window="false"
        ></config-title>
      </el-col>
      <el-col :span="8">
        <config-title
          :size="28"
          :weight="false"
          :italic="false"
          :underline="false"
          title-style="title-null"
          color="rgba(252, 79, 66, 1)"
          vertical="center"
          inner-text="9999"
          :url_type="0"
          :page_new_window="false"
          :href_new_window="false"
        ></config-title>
        <config-title
          :size="23"
          :weight="false"
          :italic="false"
          :underline="false"
          title-style="title-null"
          color="rgba(93, 129, 249, 1)"
          vertical="center"
          inner-text="月活"
          :url_type="0"
          :page_new_window="false"
          :href_new_window="false"
        ></config-title>
      </el-col>
      <el-col :span="8">
        <config-title
          :size="28"
          :weight="false"
          :italic="false"
          :underline="false"
          title-style="title-null"
          color="rgba(252, 79, 66, 1)"
          vertical="center"
          inner-text="￥9999"
          :url_type="0"
          :page_new_window="false"
          :href_new_window="false"
        ></config-title>
        <config-title
          :size="23"
          :weight="false"
          :italic="false"
          :underline="false"
          title-style="title-null"
          color="rgba(93, 129, 249, 1)"
          vertical="center"
          inner-text="营业额"
          :url_type="0"
          :page_new_window="false"
          :href_new_window="false"
        ></config-title>
      </el-col>
    </el-row>
    <el-row :gutter="0" type="flex" justify="center" align="top">
      <el-col :span="12">
        <ve-histogram
          :data="veHistogramData"
          :grid="veHistogramGrid"
          :legend="veHistogramLegend"
          height="300px"
        ></ve-histogram>
      </el-col>
      <el-col :span="12">
        <ve-line
          :data="veLineData"
          :grid="veLineGrid"
          :legend="veLineLegend"
          height="300px"
        ></ve-line>
      </el-col>
    </el-row>
    <el-data-table
      :columns="elDataTableColumns"
      :form="elDataTableForm"
      :form-attrs="elDataTableFormattrs"
      :search-form="elDataTableSearchform"
      :can-search-collapse="true"
      :single="true"
      :has-operation="true"
      :extra-buttons="elDataTableExtrabuttons"
      :header-buttons="elDataTableHeaderbuttons"
      :has-new="true"
      :has-edit="true"
      :has-view="false"
      :has-delete="true"
      new-text="新增"
      edit-text="修改"
      view-text="查看"
      :has-pagination="true"
      :dialog-attrs="elDataTableDialogattrs"
      class="material_8"
    ></el-data-table>
  </div>
</template>
<script>
export default {
  components: {},
  data: function() {
    return {
      pageName: "首页",
      veHistogramData: {
        columns: ["日期", "访问用户", "下单用户", "下单率"],
        rows: [
          {
            日期: "1/1",
            访问用户: 1393,
            下单用户: 1093,
            下单率: 32
          },
          {
            日期: "1/2",
            访问用户: 3530,
            下单用户: 3230,
            下单率: 26
          },
          {
            日期: "1/3",
            访问用户: 2923,
            下单用户: 2623,
            下单率: 76
          },
          {
            日期: "1/4",
            访问用户: 1723,
            下单用户: 1423,
            下单率: 49
          },
          {
            日期: "1/5",
            访问用户: 3792,
            下单用户: 3492,
            下单率: 32.3
          },
          {
            日期: "1/6",
            访问用户: 4593,
            下单用户: 4293,
            下单率: 78
          }
        ]
      },
      veHistogramGrid: {
        top: 35,
        bottom: 10
      },
      veHistogramLegend: {
        top: 5
      },
      veLineData: {
        columns: ["日期", "访问用户", "下单用户", "下单率"],
        rows: [
          {
            日期: "1/1",
            访问用户: 1393,
            下单用户: 1093,
            下单率: 0.32
          },
          {
            日期: "1/2",
            访问用户: 3530,
            下单用户: 3230,
            下单率: 0.26
          },
          {
            日期: "1/3",
            访问用户: 2923,
            下单用户: 2623,
            下单率: 0.76
          },
          {
            日期: "1/4",
            访问用户: 1723,
            下单用户: 1423,
            下单率: 0.49
          },
          {
            日期: "1/5",
            访问用户: 3792,
            下单用户: 3492,
            下单率: 0.323
          },
          {
            日期: "1/6",
            访问用户: 4593,
            下单用户: 4293,
            下单率: 0.78
          }
        ]
      },
      veLineGrid: {
        top: 35,
        bottom: 10
      },
      veLineLegend: {
        top: 5
      },
      elDataTableColumns: [
        {
          prop: "index",
          label: "序号"
        },
        {
          prop: "crateAt",
          label: "创建时间"
        },
        {
          prop: "updateAt",
          label: "修改时间"
        },
        {
          prop: "createBy",
          label: "创建人"
        }
      ],
      elDataTableForm: [
        {
          type: "input",
          id: "name",
          label: "单行文本",
          rules: [
            {
              required: true,
              message: "请输入单行文本",
              trigger: "blur"
            }
          ],
          el: {
            placeholder: "请输入单行文本"
          }
        }
      ],
      elDataTableFormattrs: {},
      elDataTableSearchform: [
        {
          el: {
            placeholder: "请输入"
          },
          label: "创建人",
          id: "createBy",
          type: "input"
        }
      ],
      elDataTableExtrabuttons: [
        {
          text: "查看"
        },
        {
          text: "编辑"
        },
        {
          text: "删除"
        }
      ],
      elDataTableHeaderbuttons: [
        {
          text: "新增"
        },
        {
          text: "自定义"
        }
      ],
      elDataTableDialogattrs: {
        "modal-append-to-body": false
      }
    }
  },
  mounted: function() {},
  watch: {},
  methods: {},
  destroyed: function() {}
}
</script>
<style lang="less" scoped="scoped">
.material_8 {
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  margin-top: 20px;
}
</style>
