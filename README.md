javaArrayList
=============
// PACKAGE EMPLOYEE MANAGEMENT

functions on arrayList in java
// Employee.java


package employeeManagement;

public class Employee {
	private int age = 0;
	private String Name;
	private int empId;
	private int Salary;
	
	
	
	//constructor of the type employee

	/*public Employee(String Name, String empId, String Salary)
	{
		this.Name = Name;
		this.empId = empId;
		this.Salary = Salary;
	}
	*/
	
	//constructor of the second type
	
	public Employee(String Name, int empId, int Salary, int age)
	{
		this.Name = Name;
		this.empId = empId;
		this.Salary = Salary;
		this.age = age;
	}
	 
	
	
	//setter for Employee class 
	
	void setempName (String empName)
	{
		Name = empName;
	}
	void setId(int Id)
	{
		empId = Id;
	
	}
	
	void setage(int Age)
	{
	    age = Age;
	}
	void setsalary(int salary)
	{
		Salary = salary;
	}
	
	//getters for employee class
	
	public String getName()
	{
		return Name;
	}
	public int getempId()
	{
		return empId;
	}
	public int getSalary()
	{
		return Salary;
	}
	public int getAge()
	{
		return age;
	}

}


// -------------------------------------------------------------------------------------------------------------
// -------------------------------------------------------------------------------------------------------------

// Test Employee.java

//---------------------------------------------------

package employeeManagement;
import java.util.ArrayList;

public class TestEmployee {
	
	static ArrayList<Employee> employeeList = new ArrayList<Employee> ();

	public static Employee search(int empId)
	{
		
		for(Employee emp:employeeList)
		{
			if(emp.getempId()==empId)
			{
			   return 	emp;
			}	
			
				
			
		}
		return null;
		
		
		
	}
	public static void main(String[] args) {
		
		
		 Employee emp1 = new Employee("Sumit", 755491, 8986, 21);
		 Employee emp2 = new Employee("Ravi", 755493, 9000, 22);
		 Employee emp3 = new Employee("Negi", 566663, 8452, 23);
		 Employee emp4 = new Employee("Lala", 754122, 9563, 22);
		 Employee emp5 = new Employee("Amit", 759663, 8552, 23);
		 
		 Employee emp6 = new Employee("Ajay", 788996, 5478, 22);
		 Employee emp7 = new Employee("Joshi", 455854, 7845, 22);
		 
		 employeeList.add(emp1);
		 employeeList.add(emp2);
		 employeeList.add(emp3);
		 employeeList.add(emp4);
		 employeeList.add(emp5);
		 
		 employeeList.add(emp6);
		 employeeList.add(emp7);
		 
		 
			
		 
		 
		 
		
		//System.out.println("The name of first employee is:" +emp1.getName());
		//System.out.println("Name and salary of third employee is :" +emp3.getName()+ "," +emp3.getSalary());
		
		for(Employee emp:employeeList)
		{
			
			System.out.println(" Name " +emp.getName() + " Id " +emp.getempId()+ " salary " +emp.getSalary()+ "Age" +emp.getAge());
		}
		

		Employee temp = search(755491);
		
	
		System.out.println("The id you searched for is:" +temp.getName() + ",salary is :" +temp.getSalary());
		
	}

}

