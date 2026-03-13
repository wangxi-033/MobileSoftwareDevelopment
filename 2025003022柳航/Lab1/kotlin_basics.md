# Lab1：Kotlin 基础语法练习
姓名：柳航
学号：2025003022

---

## 一、个人信息说明
[姓名] = liuhang
[学号] = 2025003022

### 参数计算
- `A` = 学号倒数第 1 位 = `2`
- `B` = 学号倒数第 2 位 = `2`
- `C` = 学号倒数第 3 位 = `0` → 按规则令其等于 `10`
- `AB` = 学号后两位组成的整数 = `22`（≥10，无需修改）
- `BC` = 学号倒数第 2、3 位组成的整数 = `20`

---

## 二、基础输出练习
### 题目 1：输出个人信息

### 答案
```kotlin
fun main() {
    val name = "liuhang"
    val studentId = "2025003022"
    println("My name is $name")
    println("My student ID is $studentId")
    println("I'm learning Kotlin!")
}

题目 3：修正编译错误
练习 3.1

### 答案
```kotlin
fun main() {
    val studentId = "2025003022"
    println("Student $studentId says hello")
}
练习 3.2
### 答案
fun main() {
    val name = "liuhang"
    println("Hello, my name is $name")
}
**练习 3.3**
### 答案
fun main() {
    val studentId = "2025003022"
    val name = "liuhang"
    println("ID: $studentId")
    println("Name: $name")
    println("Course: Kotlin")
}
**练习 3.4**
### 答案
fun main() {
    val A = 2
    println("My ID ends with $A")
}
## 题目 4：字符串模板
### 答案
fun main() {
    val numberOfMessages = 22  // AB 为你学号后两位：2025003022 → 22
    // 使用字符串模板输出通知消息
    println("You have $numberOfMessages unread messages.")
}
## 题目 5：字符串串联
### 答案
```kotlin
fun main() {
    // 声明变量：姓名拼音liuhang，学号2025003022
    val liuhangDelivery = "2025003022"
    // 使用 + 运算符进行字符串串联
    println("Package for liuhang will arrive, tracking ID: " + liuhangDelivery + ".")
}
## 题目 6：消息格式
答案：
```kotlin
fun main() {
    // 按规则替换变量
    val studentName = "liuhang"   // 姓名拼音
    val score = 22                // AB：学号后两位 22
    val bonus = 2                 // A：学号最后一位 2
    val total = score + bonus     // 计算总分

    // 使用字符串模板输出格式化消息
    println("Name: $studentName")
    println("Score: $score, Bonus: $bonus")
    println("Total: $total")
}
## 题目 7：实现基本数学运算
答案：
```kotlin
fun main() {
    // 按规则替换变量：BC=20（学号倒数第2、3位），A=2（学号最后一位）
    val operandOne = 20
    val operandTwo = 2

    // 输出所有运算结果
    println("$operandOne + $operandTwo = ${operandOne + operandTwo}")
    println("$operandOne - $operandTwo = ${operandOne - operandTwo}")
    println("$operandOne / $operandTwo = ${operandOne / operandTwo}")
    println("$operandOne * $operandTwo = ${operandOne * operandTwo}")
    println("$operandOne % $operandTwo = ${operandOne % operandTwo}")
}
## 题目 8：默认参数
答案：
```kotlin
fun main() {
    // A 替换为你学号最后一位：2
    println(liuhangGreeting(age = 2))
    // [姓名] 替换为你的姓名拼音：liuhang，B 替换为学号倒数第二位：2
    println(liuhangGreeting("liuhang", 2))
}

// 函数名替换为 liuhangGreeting，为 name 设置默认值"2025003022"
fun liuhangGreeting(name: String = "2025003022", age: Int): String {
    return "Happy Birthday, $name! You are now $age years old!"
}
## 题目 9：计步器
答案：
```kotlin
fun main() {
    // AB 替换为你学号后两位：22 → 22 * 100 = 2200
    val steps = 22 * 100
    val caloriesBurned = pedometerStepsToCalories(steps)
    println("Walking $steps steps burns $caloriesBurned calories")
}

// 重命名为符合 camelCase 的函数名和参数名
fun pedometerStepsToCalories(numberOfSteps: Int): Double {
    val caloriesBurnedForEachStep = 0.04
    val totalCaloriesBurned = numberOfSteps * caloriesBurnedForEachStep
    return totalCaloriesBurned
}
## 题目 10：比较两个数字
答案：
```kotlin
fun main() {
    // BC = 20（学号倒数第2、3位），AB = 22（学号后两位）
    val first = 20
    val second = 22

    // 使用 if/else 比较并输出较大值
    if (first > second) {
        println(first)
    } else if (second > first) {
        println(second)
    } else {
        println("First and second are equal.")
    }
}
## 题目 11：将重复代码移至一个函数中
答案：
```kotlin
fun main() {
    // 调用自定义函数输出各个城市天气
    printLiuhangWeather("Ankara", 27, 31, 82)
    printLiuhangWeather("Tokyo", 32, 36, 10)
    printLiuhangWeather("Cape Town", 59, 64, 2)
    printLiuhangWeather("Guatemala City", 50, 55, 7)
}

// 封装重复天气输出逻辑，函数名按要求命名为 printLiuhangWeather
fun printLiuhangWeather(city: String, lowTemp: Int, highTemp: Int, rainChance: Int) {
    println("City: $city")
    println("Low temperature: $lowTemp, High temperature: $highTemp")
    println("Chance of rain: $rainChance%")
    println()
}