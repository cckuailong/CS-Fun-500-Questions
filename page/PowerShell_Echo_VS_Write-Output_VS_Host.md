# PowerShell中Echo，Write-Output和Write-Host区别

## 前言

PowerShell中Echo，Write-Output和Write-Host都是输出命令，都会在控制台进行输出，那么他们有什么区别？

## 解释

- echo

echo 是 Write-Output 的别名，功能同 Write-Output

- Write-Output

写入Success输出流。这允许输出通过管道处理或重定向到文件。

- Write-Host

直接写入控制台，因此输出无法进一步处理或重定向。

## 示例

```
$a = 'Testing Write-OutPut'  | Write-Output
$b = 'Testing Write-Host' | Write-Host

Get-Variable a,b

Testing Write-Host

Name                           Value
----                           -----
a                              Testing Write-OutPut
b
```
