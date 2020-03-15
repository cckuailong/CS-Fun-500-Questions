# Mysql sql_mode中的 STRICT_TRANS_TABLES 和 STRICT_ALL_TABLES 区别

## 解释

### STRICT_TRANS_TABLES模式

- 对于InnoDB表，sql插入执行失败，会报错，全部回滚。

- 对于MyISAM表，sql插入执行失败：

1、如果是第一行数据出错，则会报错，会回滚

2、如果是大于第一行数据出错，MySQL将非法值转换为最接近该列的合法值并插入调整后的值。如果不能转换，MySQL在列中插入隐式默认值。在任何情况下，MySQL都不会报错（除非语法错误），并会继续执行语句。

### STRICT_ALL_TABLES模式

- 对于InnoDB表，和STRICT_TRANS_TABLES模式相同

- 对于MyISAM表，sql插入执行失败会保存错误发生之前修改的行，忽略剩下的行，并报错。

## 总结

- 对于InnoDB表，STRICT_TRANS_TABLES与STRICT_ALL_TABLES模式效果一样，插入报错就全部回滚。

- 对于MyISAM表

1. STRICT_TRANS_TABLES：

    (1) 插入第一行数据失败会报错，会回滚并且停止。

    (2) 大于第一行之后的插入数据失败，mysql会把不合法的值强转为最为接近的值 或者隐式默认值，并且不会报错。

2. STRICT_ALL_TABLES：如果插入执行失败会保存错误发生之前插入的行，忽略剩下的行，并报错。
