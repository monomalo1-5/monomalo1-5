import java.util.Scanner

fun main() {
    val scanner = Scanner(System.`in`)
    var continuar = true
    
    while (continuar) {
        println("Ingrese el primer número:")
        val numero1 = scanner.nextDouble()
        
        println("Ingrese el segundo número:")
        val numero2 = scanner.nextDouble()
        
        println("Seleccione la operación:")
        println("1. Suma")
        println("2. Resta")
        println("3. Multiplicación")
        println("4. División")
        val opcion = scanner.nextInt()
        
        when (opcion) {
            1 -> println("La suma es: ${numero1 + numero2}")
            2 -> println("La resta es: ${numero1 - numero2}")
            3 -> println("La multiplicación es: ${numero1 * numero2}")
            4 -> {
                if (numero2 != 0.0) {
                    println("La división es: ${numero1 / numero2}")
                } else {
                    println("No se puede dividir por cero.")
                }
            }
            else -> println("Opción inválida")
        }
        
        println("¿Desea realizar otra operación? (si/no)")
        val respuesta = scanner.next()
        if (respuesta.toLowerCase() != "si") {
            continuar = false
        }
    }
    println("¡Gracias por usar la calculadora!")
}
