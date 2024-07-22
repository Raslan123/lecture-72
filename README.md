# lecture-72
#include <iostream>
#include <unordered_map>
using namespace std;

int main() {
    // Create an unordered_map to store string keys and integer values
    unordered_map<string, int> hashTable;

    // Insert key-value pairs into the hash table
    hashTable["apple"] = 1;
    hashTable["banana"] = 2;
    hashTable["cherry"] = 3;

    // Access values using keys
    cout << "apple: " << hashTable["apple"] << endl;
    cout << "banana: " << hashTable["banana"] << endl;

    // Check if a key exists
    if (hashTable.find("cherry") != hashTable.end()) {
        cout << "cherry is found with value: " << hashTable["cherry"] << endl;
    } else {
        cout << "cherry is not found" << endl;
    }

    // Remove a key-value pair
    hashTable.erase("banana");

    // Iterate over all key-value pairs
    for (const auto& pair : hashTable) {
        cout << pair.first << ": " << pair.second << endl;
    }

    return 0;
}
