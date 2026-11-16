import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter the number of students: ");
        int n = scanner.nextInt();
        scanner.nextLine(); // Consume the newline

        Student[] students = new Student[n];

        for (int i = 0; i < n; i++) {
            System.out.println("Enter details for student " + (i + 1) + ":");
            System.out.print("USN: ");
            String usn = scanner.nextLine();
            System.out.print("Name: ");
            String name = scanner.nextLine();
            System.out.print("Branch: ");
            String branch = scanner.nextLine();
            System.out.print("Phone: ");
            String phone = scanner.nextLine();

            students[i] = new Student(usn, name, branch, phone);
        }

        
        System.out.println("\nStudent Details:");
        System.out.printf("%-10s %-20s %-15s %-15s%n", "USN", "Name", "Branch", "Phone");
        System.out.println("-------------------------------------------------------------");
        for (Student student : students) {
            student.displayDetails();
        }

        scanner.close();
    }
}
