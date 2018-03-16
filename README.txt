# slimes

package validator;
import java.util.regex.Pattern;
import java.util.regex.Matcher;
import java.util.Scanner;

public class Validator1 {
    
   
    static Scanner input = new Scanner(System.in);
    public static void main(String[] args) {
        
        Validator validator = new Validator();
        PhoneNumber phoneNumberValidator = new PhoneNumber();
        
        String SaNumber;
        String EmailDomain;
        System.out.println("Enter your phone number");
        SaNumber = input.next();
        System.out.println("Enter Email");
        EmailDomain = input.next();
       

        if(phoneNumberValidator.numberIsValid(SaNumber) )
            System.out.println("Valid Numbers");
        else
            System.out.println("Invalid Numbers");
        
        System.out.println();
         
        if(validator.isValid(EmailDomain))
            System.out.println("Your Email is Valid");
        else
            System.out.println("Your Email is Invalid");
        
    }
    
}

=======================================================

package validator;

import java.util.regex.Pattern;

 public class PhoneNumber {
    
      public static boolean numberIsValid(String numbers)
    {
       String phoneNumberRegex = "^((?:\\+27|27)|0)(=72|82|73|83|74|84|071|60)+(\\d{7})$";
               
                             
        Pattern obj = Pattern.compile(phoneNumberRegex);
        if (numbers == null)
            return false;
        return obj.matcher(numbers).matches();
    }
}

=========================================================
package validator;

import java.util.Scanner;
import java.util.regex.Pattern;


public class Validator {
      public static boolean isValid(String domain)
    {
        String domainRegex = "^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+.[a-zA-Z0-9-.]+.[a-zA-Z0-9-.]+$";
                                  
        Pattern obj = Pattern.compile(domainRegex);
        if (domain == null)
            return false;
        return obj.matcher(domain).matches();
    }
      
      
      public static boolean SAnumberIsValid(String SAnumbers)
    {
       String SAphoneNumbersRegex = "^((?:\\+27|27)|0)(=72|82|73|83|74|84|071|60)+(\\d{7})$";
               
                             
        Pattern obj = Pattern.compile(SAphoneNumbersRegex);
        if (SAnumbers == null)
            return false;
        return obj.matcher(SAnumbers).matches();
    }
    
}
