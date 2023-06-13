#include <iostream>

int main() {
    bool doors[100] = { false }; // создаем массив дверей, изначально все закрыты
    for (int i = 1; i <= 100; i++) { // проходим по каждой двери
        for (int j = i - 1; j < 100; j += i) { // проходим по каждой i-той двери и меняем ее состояние
            doors[j] = !doors[j];
        }
    }
    for (int i = 0; i < 100; i++) { // выводим состояние каждой двери
        std::cout << "Дверь " << i + 1 << ": " << (doors[i] ? "open" : "закрыта") << std::endl;
    }
    return 0;
}