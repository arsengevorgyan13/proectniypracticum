#include <iostream>
#include <string>
#include <vector>

//попробовать getline для этой штуки

int main() {
	std::vector<char> myvector;
	std::string word;
	std::cout << "Enter a string: ";
	std::cin >> word;
	std::cout << "1. Insert" << std::endl;
	std::cout << "2. Erase" << std::endl;
	std::cout << "3. Replace" << std::endl;
	std::cout << "4. Find" << std::endl;
	int option;
	while (true){
		std::cout << std::endl;
		std::cout << "Choose an option(1-4): ";
		option = 0;
		std::cin >> option;
		if (!option) {
			break;
		}
		std::string message;
		int index;
		int quantity;
		switch (option) {
		case 1:
			std::cout << "Index: ";
			std::cin >> index;
			std::cout << "String: ";
			std::cin >> message;
			word.insert(index, message);
			std::cout << "word = " << word;
			break;
		case 2:
			std::cout << "Index: ";
			std::cin >> index;
			std::cout << "Quantity: ";
			std::cin >> quantity;
			word.erase(index, quantity);
			std::cout << "word = " << word;
			break;
		case 3:
			std::cout << "Index: ";
			std::cin >> index;
			std::cout << "Quantity: ";
			std::cin >> quantity;
			std::cout << "String: ";
			std::cin >> message;
			word.replace(index, quantity, message);
			std::cout << "word = " << word;
			break;
		case 4:
			std::cout << "String: ";
			std::cin >> message;
			index = word.find(message);
			if (index != -1) {
				std::cout << "index = " << word;
			}
			else {
				std::cout << "string not found :/";
			}
			break;
}
	}
}
