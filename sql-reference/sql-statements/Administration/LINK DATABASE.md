# LINK DATABASE

## 功能

**（已废弃！！！）**
该语句用户链接一个逻辑集群的数据库到另外一个逻辑集群, 一个数据库只允许同时被链接一次，删除链接的数据库

并不会删除数据，并且被链接的数据库不能被删除, 需要管理员权限

## 语法

```sql
LINK DATABASE src_cluster_name.src_db_name des_cluster_name.des_db_name
```

## 示例

1. 链接 test_clusterA 中的 test_db 到 test_clusterB, 并命名为 link_test_db

    ```sql
    LINK DATABASE test_clusterA.test_db test_clusterB.link_test_db;
    ```

2. 删除链接的数据库 link_test_db

    ```sql
    DROP DATABASE link_test_db;
    ```
