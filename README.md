#include <iostream>

// Функція для обчислення найбільшого спільного дільника за алгоритмом Евкліда
int euclideanAlgorithm(int a, int b) {
    while (b != 0) {
        int temp = b;  // Зберігаємо значення b для подальшого використання
        b = a % b;     // Оновлюємо b, знаходячи залишок від ділення a на b
        a = temp;      // Оновлюємо a значенням, яке було збережено в temp
    }
    return a;         // Повертаємо результат - найбільший спільний дільник
}

int main() {
    int num1, num2;
    std::cout << "Введіть перше число: ";
    std::cin >> num1;
    std::cout << "Введіть друге число: ";
    std::cin >> num2;

    int gcd = euclideanAlgorithm(num1, num2);  // Викликаємо функцію для знаходження НСД

    std::cout << "Найбільший спільний дільник: " << gcd << std::endl;

    return 0;
}
