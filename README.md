# hotamjon-aminov

package com.example.aquarium

fun main() {
    RandomArticle().random()
}

class RandomArticle{
    val articles = arrayOf(
        "article_1",
        "article_2",
        "article_3",
        "article_4",
        "article_5"
    )

    fun random() {
        val randomArticle = articles.random()
        println(randomArticle)
    }
}
