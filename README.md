Aggregation in Java — Simple Format
Aggregation is a HAS-A relationship between two classes.

One class contains an object of another class.

The contained object can exist independently.

Example: A Department has an Employee.

Simple Program
java
// Employee class
class Employee {
    int id;
    String name;

    Employee(int id, String name) {
        this.id = id;
        this.name = name;
    }
}

// Department class has an Employee
class Department {
    String deptName;
    Employee emp;   // Aggregation

    Department(String deptName, Employee emp) {
        this.deptName = deptName;
        this.emp = emp;
    }

    void display() {
        System.out.println("Department: " + deptName);
        System.out.println("Employee ID: " + emp.id);
        System.out.println("Employee Name: " + emp.name);
    }
}

public class AggregationExample {
    public static void main(String[] args) {
        Employee e1 = new Employee(101, "Rahul");
        Department d1 = new Department("IT", e1);

        d1.display();
    }
}
