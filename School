using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace School
{
   public class Student:School
    {
        public string StudentName { get; set; }
        public int StudentNumber { get; set; }

        public Student(string name, int studentNumber)
        {
           this.StudentName = name;
           this.StudentNumber = studentNumber;
        }

       
    }

   public class Course
    {
        public string CourseName { get; set; }
        public List<Student> courseStudents = new List<Student>(28);
        public Course(string name)
        {
            this.CourseName = name;
        }


        public void AddStudent(Student student)
        {
            if (IsListIsFull() == false)
            {
                courseStudents.Add(student);
            }
        }

        public void RemoveStudent(Student student)
        {
            courseStudents.Remove(student);
        }

        public bool IsListIsFull()
        {
            if (this.courseStudents.Count > 28)
            {
                throw new ArgumentOutOfRangeException("The list is full");
            }
            return false;
        }

        public void ListStudents()
        {
            Console.WriteLine("Course name: {0}", CourseName);
            foreach (Student Stud in courseStudents)
            {
                Console.WriteLine("Student name: {0}", Stud.StudentName);
                Console.WriteLine("Student number: {0}", Stud.StudentNumber);
            }

        }
    }


   public class School
    {
        public List<Student> studentsList = new List<Student>();

        public bool IsStudentNumberExists(int number)
        {
            foreach (Student Stud in studentsList)
            {
                if (Stud.StudentNumber == number)
                {
                    return true;
                }
            }
            return false;
        }

        public bool IsStudentNumberInRange(int number)
        {
            if (number < 10000 || number > 99999)
            {
                return false;
            }
            return true;
        }

        static void Main(string[] args)
        {

            string name;
            int number;

            School school = new School();
            Course cr = new Course("GF");
            name = "Pesho";
            number = 11111;
         
            school.studentsList.Add(new Student("Pesho", 11111));
            school.studentsList.Add(new Student("rPesho", 21111));
            school.studentsList.Add(new Student("GPesho", 31111));

            cr.IsListIsFull();
            cr.AddStudent(new Student("GPesho", 31111));
            cr.IsListIsFull();
            cr.AddStudent(new Student("GPesho", 31111));
            cr.ListStudents();
           
        }
    }


}
