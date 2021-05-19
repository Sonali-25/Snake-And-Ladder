package com.empwage.builder;

import java.util.HashMap;
import java.util.Map;
import java.util.Random;
import java.util.Scanner;

import javax.lang.model.util.ElementScanner6;

public class EmployeeWageCalculator {

	public static void main(String[] args) {
		EmployeeNWage employee = new EmployeeNWage();
		employee.startWageCalculation();
	}

}

class EmployeeNWage
{
	
	final static int STOPHRS = 100;
    final static int STOPDAYS = 20;
    static int workingdays = 0, workinghrs = 0;
	
	
	public int attendance()
	{
		int isAbsent = 0;
		Random r = new Random();
		isAbsent=r.nextInt(2);
		return isAbsent;
	}
	
	public void startWageCalculation()
	{
        System.out.println("Welcome to Employee Wage Computation Program");
        wageCalculator();
    }
        

    public void wageCalculator()
    {
        System.out.println("To check attendance and proceed wage calculation Enter 1");
        Scanner s = new Scanner(System.in);
        int checkAttendance = s.nextInt();
        if(checkAttendance == 1)
        {
            int todayAttendance = attendance();
        switch(todayAttendance)
        {
            case 0:
                System.out.println("Employee is absent today");
                System.out.println("Working Days: "+workingdays+"\nWorking Hours: "+workinghrs);
                wageCalculator();
                
                break;
            case 1:
                System.out.println("Employee is present today");
                System.out.println("Enter yes if working overtime else no");
                String overtime = s.next();
                if("yes".equals(overtime))
                {
                    workingdays = workingdays+1;
                    workinghrs = workinghrs+16;
                }
                else{
                    workingdays = workingdays+1;
                    workinghrs = workinghrs+8;
                }
                if(monthCovered(workingdays, workinghrs))
                {
                    System.out.println("Wage: "+100*20 +" Ruppes");
                    System.out.println("Working Days: "+workingdays+"\nWorking Hours: "+100);
                    break;   
                }
                else{
                    System.out.println("Working Days: "+workingdays+"\nWorking Hours: "+workinghrs);
                    wageCalculator(); 
                }
                 
            default:
                break;

        }

        }
        else{
            System.out.println("Enter 1 only to proceed for wage Calculation");
        }
        
    }
		
	public boolean monthCovered(int workingdays,int workinghrs)
	{
        if(workingdays==STOPDAYS | workinghrs>=STOPHRS)
        {
            return true;
        }
		else
        {
            return false;
        }
	}
	
}



