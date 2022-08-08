# self-Understanding
+ 只要在源码中有import package的语句，无论该package有没有被显式使用，该pacakge中的`func init`都会执行
1. sql驱动的注册 `import "github.com/go-sql-driver/mysql"`
    + mysql包下的driver.go文件中有init方法完成驱动注册
    + ```
      func init() {
            sql.Register("mysql", &MySQLDriver{})
      }
 
