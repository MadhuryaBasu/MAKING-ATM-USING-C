# MAKING-ATM-USING-C
#include <stdio.h>

int main() {
    int pin;
	 // Set PIN number
    int user_pin;
  
    printf("\n ATM created BY Mis Madhurya Basu");
     printf("\n ______________________________________");
     printf("\n SWAP YOUR ATM CARD");
     printf("\n SELECT ACCOUNT TYPE");
     
        printf("\nChoose an option:\n");
        printf("1. Savings Account\n");
        printf("2. Current Account\n");
        printf("3. Salary Account\n");
       
       
    float balance = 5000.0; // Set initial balance
    int option;
    float amount;
    
    printf("\n Welcome to ICICI BANK :\n");
    printf("\n ________________________\n");
    printf("\n- Welcome to the ATM machine-\n");
    printf("\n Enter your PIN: ");
    scanf("%d", &user_pin);

   
    while (1) {
        printf("\nChoose an option:\n");
        printf("1. View balance\n");
        printf("2. Deposit money\n");
        printf("3. Withdraw money\n");
        printf("4. Exit\n");
        scanf("%d", &option);

        switch (option) {
            case 1:
                printf("Your account balance is: $%.2f\n", balance);
                break;
            case 2:
                printf("Enter the amount you want to deposit: $");
                scanf("%f", &amount);
                balance += amount;
                printf("Your new balance is: $%.2f\n", balance);
                break;
            case 3:
                printf("Enter the amount you want to withdraw: $");
                scanf("%f", &amount);
                if (amount > balance) {
                    printf("Insufficient funds\n");
                } else {
                    balance -= amount;
                    printf("Your new balance is: $%.2f\n", balance);
                }
                break;
            case 4:
                printf("Thank you for using the ATM machine\n");
                printf("VISIT AGAIN");
                return 0;
            default:
                printf("Invalid option\n");
                break;
        }
    }
}
