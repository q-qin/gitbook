### [vue官方风格指南](https://cn.vuejs.org/v2/style-guide/)

### 基本结构

    <template>
    <div></div>
    </template>
    <script>
    export default {
        components: {},
        data() {
        return {};
        },
        methods: {},
        mounted() {}
    };
    </script>
    <!-- 声明语言，并且添加scoped -->
    <style lang="scss" scoped></style>

### vue文件方法声明顺序

    - data
    - components
    - props
    - computed
    - watch
    - created
    - mounted
    - activited
    - update
    - beforeRouteUpdate
    - metods

### 标签属性自动换行（对除第一个属性外的其他每个属性进行换行，并保持对齐），如
    <nv-uploader
        target="/Common/UploadHandler.ashx?path=ht"
        ref="uploader"
        @start="startUpload"
        @finish="finishUpload"
        @progress="progress"
        :maxSize="5*1024*1024"
        :maxCount="3"
        @error="error"
      ></nv-uploader>

### 组件命名规范（始终是多个单词的，有意义的名词、简短、具有可读性）
   
   - 导入及注册组件时，遵循 PascalCase(单词首字母大写命名) 约定,如
   `import NvUploader form '@/components/nvUploader.vue'`
   - 使用组件需要前后闭合，并以短线分隔，如
   `<nv-uploader ...></nv-uploader>`
   - 必须符合自定义元素规范: **切勿使用保留字**


### props 命名规范
   - 在声明 prop 的时候，其命名应该始终使用 camelCase，而在模板中应该始终使用 kebab-case，如
   
    <script>
    props: {
        greetingText : {
            type : String,
            default : '',
        }
    }
    </script>

    <welcome-message greeting-text="hi"></welcome-message>
    
