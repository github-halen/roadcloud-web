<script>
export default {
  name: 'MenuItem',
  functional: true,
  props: {
    icon: {
      type: String,
      default: ''
    },
    title: {
      type: String,
      default: ''
    }
  },
  render(h, context) {
    const { icon, title } = context.props
    // const { icon, title } = '[{"path":"https://github.com/elunez/eladmin","component":"Layout","children":[{"path":"https://github.com/elunez/eladmin","meta":{"title":"项目地址","icon":"github"}}]},{"name":"系统管理","path":"/system","redirect":"noredirect","component":"Layout","alwaysShow":true,"meta":{"title":"系统管理","icon":"system"},"children":[{"name":"用户管理","path":"user","component":"system/user/index","meta":{"title":"用户管理","icon":"peoples"}},{"name":"角色管理","path":"role","component":"system/role/index","meta":{"title":"角色管理","icon":"role"}},{"name":"权限管理","path":"permission","component":"system/permission/index","meta":{"title":"权限管理","icon":"permission"}},{"name":"菜单管理","path":"menu","component":"system/menu/index","meta":{"title":"菜单管理","icon":"menu"}},{"name":"部门管理","path":"dept","component":"system/dept/index","meta":{"title":"部门管理","icon":"dept"}},{"name":"岗位管理","path":"job","component":"system/job/index","meta":{"title":"岗位管理","icon":"Steve-Jobs"}},{"name":"字典管理","path":"dict","component":"system/dict/index","meta":{"title":"字典管理","icon":"dictionary"}}]},{"name":"系统监控","path":"/monitor","redirect":"noredirect","component":"Layout","alwaysShow":true,"meta":{"title":"系统监控","icon":"monitor"},"children":[{"name":"操作日志","path":"logs","component":"monitor/log/index","meta":{"title":"操作日志","icon":"log"}},{"name":"异常日志","path":"errorLog","component":"monitor/log/errorLog","meta":{"title":"异常日志","icon":"error"}},{"name":"系统缓存","path":"redis","component":"monitor/redis/index","meta":{"title":"系统缓存","icon":"redis"}},{"name":"SQL监控","path":"druid","component":"monitor/sql/index","meta":{"title":"SQL监控","icon":"sqlMonitor"}},{"name":"实时控制台","path":"msg","component":"monitor/log/msg","meta":{"title":"实时控制台","icon":"codeConsole"}}]},{"name":"系统工具","path":"/sys-tools","redirect":"noredirect","component":"Layout","alwaysShow":true,"meta":{"title":"系统工具","icon":"sys-tools"},"children":[{"name":"定时任务","path":"timing","component":"system/timing/index","meta":{"title":"定时任务","icon":"timing"}},{"name":"代码生成","path":"generator","component":"generator/index","meta":{"title":"代码生成","icon":"dev"}},{"name":"接口文档","path":"swagger2","component":"tools/swagger/index","meta":{"title":"接口文档","icon":"swagger"}},{"name":"邮件工具","path":"email","component":"tools/email/index","meta":{"title":"邮件工具","icon":"email"}},{"name":"图床管理","path":"pictures","component":"tools/picture/index","meta":{"title":"图床管理","icon":"image"}},{"name":"七牛云存储","path":"qiniu","component":"tools/qiniu/index","meta":{"title":"七牛云存储","icon":"qiniu"}},{"name":"支付宝工具","path":"aliPay","component":"tools/aliPay/index","meta":{"title":"支付宝工具","icon":"alipay"}}]},{"name":"组件管理","path":"/components","redirect":"noredirect","component":"Layout","alwaysShow":true,"meta":{"title":"组件管理","icon":"zujian"},"children":[{"name":"图标库","path":"icon","component":"components/IconSelect","meta":{"title":"图标库","icon":"icon"}},{"name":"富文本","path":"tinymce","component":"components/Editor","meta":{"title":"富文本","icon":"fwb"}},{"name":"Markdown","path":"markdown","component":"components/MarkDown","meta":{"title":"Markdown","icon":"markdown"}},{"name":"Yaml编辑器","path":"yaml","component":"components/YamlEdit","meta":{"title":"Yaml编辑器","icon":"dev"}}]},{"name":"多级菜单","path":"/nested","redirect":"noredirect","component":"Layout","alwaysShow":true,"meta":{"title":"多级菜单","icon":"menu"},"children":[{"name":"二级菜单1","path":"menu1","redirect":"noredirect","component":"nested/menu1/index","alwaysShow":true,"meta":{"title":"二级菜单1","icon":"menu"},"children":[{"name":"三级菜单1","path":"menu1-1","component":"nested/menu1/menu1-1","meta":{"title":"三级菜单1","icon":"menu"}},{"name":"三级菜单2","path":"menu1-2","component":"nested/menu1/menu1-2","meta":{"title":"三级菜单2","icon":"menu"}}]},{"name":"二级菜单2","path":"menu2","component":"nested/menu2/index","meta":{"title":"二级菜单2","icon":"menu"}}]},{"name":"商品管理","path":"/commodity","redirect":"noredirect","component":"Layout","alwaysShow":true,"meta":{"title":"商品管理","icon":"menu"},"children":[{"name":"品牌管理","path":"brand","redirect":"noredirect","component":"commodity/brand/index","alwaysShow":true,"meta":{"title":"品牌管理","icon":"menu"}},{"name":"商品类型","path":"menu2","component":"nested/menu2/index","meta":{"title":"商品类型","icon":"menu"}}]}]';
    // console.log(context.props);
    const vnodes = []

    if (icon) {
      vnodes.push(<svg-icon icon-class={icon}/>)
    }

    if (title) {
      vnodes.push(<span slot='title'>{title}</span>)
    }
    return vnodes
  }
}
</script>
