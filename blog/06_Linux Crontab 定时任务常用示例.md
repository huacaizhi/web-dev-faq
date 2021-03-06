### Linux Crontab 定时任务常用示例

#### 查看定时任务`crontab -l`
#### 编辑定时任务`crontab -e`
#### crontab 格式: 秒 分 时 日 月 周 
#### `*`代表任何可能的值,即通配符

每天凌晨2点  `0 0 2 * * *`和每天隔一小时 `0 * */1 * * *`

例1：每隔5秒执行一次：`*/5 * * * * *`

例2：每隔5分执行一次：`0 */5 * * * *`

在26分、29分、33分执行一次：`0 26,29,33 * * * *`

例3：每天半夜12点30分执行一次：`0 30 0 * * *` （注意日期域为0不是24）

每天凌晨1点执行一次：`0 0 1 * * *`

每天上午10：15执行一次： `0 15 10 * * *` 或 `0 15 10 * * *` 或 `0 15 10 * * * *`

每天中午十二点执行一次：`0 0 12 * * *`

每天14点到14：59分，每1分钟执行一次：`0 * 14 * * *`

每天14点到14：05分，每1分钟执行一次：`0 0-5 14 * * *`

每天14点到14：55分，每5分钟执行一次：`0 0/5 14 * * *`

每天14点到14：55分，和18点到18点55分，每5分钟执行一次：`0 0/5 14,18 * * *`

每天18点执行一次：`0 0 18 * * *`

每天18点、22点执行一次：`0 0 18,22 * * *`

每天7点到23点，每整点执行一次：`0 0 7-23 * * *`

每个整点执行一次：`0 0 0/1 * * *`