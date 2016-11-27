# Vectors
Describe 2 or more vectors using Java

package com.company;
     class Vector implements Comparable<Vector> {
        double a, b; //начало и конец вектора
        public Vector(double A, double B) {//начало конструктора
            this.a = A;
            this.b = B;
        }//конец конструктора
        double lenght() {//находит длину конструктора 
            return b - a;
        }
        public int compareTo(Vector a) {//метод сравнения
            if (this.lenght() > a.lenght())
                return 1;
            else if ((this.lenght() < a.lenght()))
                return -1;
            else return 0;
        }
    }
        public class Main {
            public static void main(String[] args) {
                Vector v1 = new Vector(0, 2.3);//первый вектор
                Vector v2 = new Vector(1.1, 3.4);//второй вектор
                if (v1.lenght() > v2.lenght())
                    System.out.println("The 1st vector is longer than the 2nd one");
                else if(v1.lenght() < v2.lenght())
                    System.out.println("The 2nd vector is longer than the 1st one");
                else System.out.println("They are equal");
                System.out.println(v1.compareTo(v2));//выводит результат сравнения
            }
        }
