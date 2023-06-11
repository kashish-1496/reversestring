#include <stdio.h>

void reverseString(char str[]) {
    int length = 0;
    int i;
    char temp;
    
    // Calculate the length of the string
    while (str[length] != '\0') {
        length++;
    }
    
    // Swap characters to reverse the string
    for (i = 0; i < length / 2; i++) {
        temp = str[i];
        str[i] = str[length - i - 1];
        str[length - i - 1] = temp;
    }
}

int main() {
    char input[100];

    printf("Enter a string: ");
    scanf("%s", input);
    
    reverseString(input);
    
    printf("Reversed string: %s\n", input);
    
    return 0;
}
