# hotamjon-aminov

package com.example.myapplicationd

import java.math.RoundingMode
import java.text.DecimalFormat

fun main() {
    println("Hello, world!!!")

    println("Введите день недели: ")
    val listenDay = readLine()!!.toInt()
    val dayName = dayOfTheWeek(listenDay)
    println(dayName)

    println("Введите стоимость 1 кг яблок: ")
    val listenApple = readLine()!!.toInt()
    apples(listenApple)

    println("Введите число N: ")
    val numberN = readLine()!!.toDouble()
    number(numberN)
}

fun dayOfTheWeek (int: Int): String {
    val days: Array<String> = arrayOf("Понедельник", "Вторник", "Среда", "Четверг", "Пятница", "Суббота", "Воскресенье")
    val i = int - 1
    val n = days[i]
    return n
}

fun apples (int: Int) {
    val i = int
    var oneKg: Double = 0.0

    while (oneKg < 0.9) {
        val dec = DecimalFormat("##.#")
        dec.roundingMode = RoundingMode.CEILING

        oneKg += 0.1
        val cost = oneKg * i
        println(dec.format(cost))
    }
}

fun number (double: Double) {
    val N: Double = double
    var p: Double = 1.0
    var start: Double = 1.0

    val dec = DecimalFormat("##.###")
    dec.roundingMode = RoundingMode.CEILING

    while (start <= N){


        start += 0.1
        for (i in 1..N.toInt()) {
            p = p * (1 + 0.1 * i)
        }
    }
    println("Result=${dec.format(p)}")
}

