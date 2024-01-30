package Account;
import java.util.*;

class Account
{
	int CN;
	int PN;
	void setCustomerNumber(int cn)
	{
		CN = cn;
		//System.out.println(CN);
	}
	void setPinNumber(int pn)
	{
		PN = pn;
		//System.out.println(PN);
	}
	int getCustomerNumber()
	{
		return CN;
	}
	int getPinNumber()
	{
		return PN;
	}
}
class Option_menu_11 extends Account
{
	Scanner input = new Scanner(System.in);
	HashMap<Integer, Integer> data = new HashMap<Integer, Integer>();
	void getLogin()
	{
		int i = 125;
		do
		{
			try
			{
				data.put(11111, 111);
				data.put(11112, 222);
				data.put(11113, 333);
				data.put(11114, 444);
				data.put(11115, 555);
				
				System.out.println("WELCOME TO THE VKP ATM");
				
				System.out.println("Enter your CUSTOMER NUMBER");
				setCustomerNumber(input.nextInt());
				
				System.out.println("Enter your PIN NUMBER");
				setPinNumber(input.nextInt());
				
				int A = getCustomerNumber();
				int B = getPinNumber();
				
				if(data.containsKey(A) && data.get(A) == B)
				{
					getAccountType();
					
				}
				else
				{
					System.out.println("Login UNSUCCESFUL");
				}
			}
			catch(InputMismatchException h)
			{
				System.out.println("Please Enter ONLY Numbers");
				System.out.println("CHARACTERS & SYMBOLS are NOT allowed");
				i = 450;
			}
			
		}while(i == 125);
	}
	void getAccountType()
	{
		System.out.println("SELECT THE ACCOUNT TYPE THAT YOU WANT TO ACCESS");
		System.out.println("Type 1 : CURRENT ACCOUNT");
		System.out.println("Type 2 : SAVING ACCOUNT");
		System.out.println("Type 3 : EXIT");
		System.out.println("Choice : ");
		
		int Choice = input.nextInt();
		
		switch(Choice)
		{
		case 1 : 
			getCurrent();
			break;
			
		case 2 :
			getSaving();
			break;
			
		case 3 :
			System.out.println("THANK YOU FOR USING THIS ATM, VISIT AGAIN");
			break;
			
		default :
			System.out.println("Invalid Choice.");
			System.out.println("Please Enter valid Choice.");
			break;
		}
		
	}
	void getCurrent()
	{
		System.out.println("CURRENT Account");
		System.out.println("Type 1 : VIEW BALANCE");
		System.out.println("Type 2 : WITHDRAW FUNDS");
		System.out.println("Type 3 : DEPOSIT ACCOUNT");
		System.out.println("Type 4 : EXIT ");
		System.out.println("CHOICE : ");
		
		int Choice = input.nextInt();
		switch(Choice)
		{
		
		case 1 :
			break;
			
		case 2 :
			break;
			
		case 3 :
			break;
			
		case 4 :
			System.out.println("THANK YOU FOR USING THIS ATM, VISIT AGAIN");
			break;
			
		default :
			System.out.println("Invalid Choice.");
			System.out.println("Please Enter valid Choice.");
			break;
			
		
		}
	}
	void getSaving()
	{
		System.out.println("Saving Account");
		System.out.println("Type 1 : VIEW BALANCE");
		System.out.println("Type 2 : WITHDRAW FUNDS");
		System.out.println("Type 3 : DEPOSIT ACCOUNT");
		System.out.println("Type 4 : EXIT");
		System.out.println("CHOICE : ");
		
		int Choice = input.nextInt();
		switch(Choice)
		{
		
		case 1 :
			break;
			
		case 2 :
			break;
			
		case 3 :
			break;
			
		case 4 :
			System.out.println("Thank You for using this ATM, VISIT AGAIN");
			break;
			
		default :
			System.out.println("Invalid Choice.");
			System.out.println("Please Enter valid Choice.");
			break;
		}
	}
}
public class ATM_1108
{
		public static void main(String[] args)
		{
			Option_menu_11 op = new Option_menu_11();
			op.getLogin();
		}
}

