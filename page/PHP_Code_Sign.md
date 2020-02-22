# PHP 代码标记风格

## 解释

目前有 4 中标记风格

### XML标签

```
<?php
    phpinfo();
 ?>
```

- php推荐使用的标记风格
- 服务器管理员无法禁用，所有服务器上均可使用该风格。

### 脚本标签

```
<script language="php">
    phpinfo();
</script>
```

- 默认开启，无法禁用
- 此种风格中，language的值，大小写都可以

### 短标签

```
<?
    phpinfo();
?>
```

- 此种风格需要在配置文件php.ini中启用short_open_tage选项
- 此种风格在许多环境中默认是不支持的

### ASP标签

```
<%
    phpinfo();
%>
```

- 此种风格需要在配置文件php.ini中启用asp_tag选项
- 在默认情况下是禁用的
