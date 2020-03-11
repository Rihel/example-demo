<template>
  <div>
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
    ></el-data-table>
  </div>
</template>
<script>
export default {
  components: {},
  data: function() {
    return {
      pageName: "系统管理",
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
<style lang="less" scoped="scoped"></style>
