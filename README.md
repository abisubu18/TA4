
public class SavingsAccount extends BankAccount { //SavingsAccount is a subclass (child) of BankAccount
	
	private double annualInterestRate; //Instance variable for annualInterestRate
	private double minimumBalance; //Instance variable for minimumBalance
	
	public double balance1;
	
	public SavingsAccount() { //Default constructor for SavingsAccount
		annualInterestRate = 0.05;
		minimumBalance = 0.0;
	}
	
	public SavingsAccount (double AIR, double minB) { //Constructor for SavingsAccount
		
		this.annualInterestRate = AIR;
		this.minimumBalance = minB;	
	}
	
	
	public void depositMonthlyInterest() { //method to deposit monthly interest
		super.deposit(annualInterestRate/12 * super.getBalance());
	}

	
	public void setAnnualInterestRate(double d) { // mutator method to set annual interest rate
		if (d < 0 || d > 1) {
			annualInterestRate = annualInterestRate;
		}
		else {
			annualInterestRate = d;
		}
	}

	public double getAnnualInterestRate() { //accessor method to get annual interest rate
		
		return annualInterestRate;
	}

	public void setMinimumBalance(double d) { //mutator method to set minimum balance
		minimumBalance = d;
	}
	
	public double getMinimumBalance() { //accessor method to get minimum balance
		
		return minimumBalance;
	}
	
	public void withdraw (double newWithdraw) { //override and use parent class withdraw method
		if (super.getBalance() - newWithdraw >= minimumBalance) {
			super.withdraw(newWithdraw);
		}
	}
	
	// TA4 additions 
	
	public SavingsAccount(double annualInterestRate){
		
	}
	public SavingAccount(Customer accountHolder, double balance, double annaulInterestRate){
		
	}

}
