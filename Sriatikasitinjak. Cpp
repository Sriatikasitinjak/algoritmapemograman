#include <iostream>
#include <string>
using namespace std;

struct Student {
    int npm;
    string name;
    int nilaiUts;
    int nilaiSemester;
    float nilaiAkhir;
    char nilaiHuruf;
};

void calculateFinalScore(Student &student) {
    student.nilaiAkhir = (0.4 * student.nilaiUts) + (0.6 * student.nilaiSemester);
    if (student.nilaiAkhir >= 80) {
        student.nilaiHuruf = 'A';
    } else if (student.nilaiAkhir >= 70) {
        student.nilaiHuruf = 'B';
    } else if (student.nilaiAkhir >= 55) {
        student.nilaiHuruf = 'C';
    } else if (student.nilaiAkhir >= 40) {
        student.nilaiHuruf = 'D';
    } else {
        student.nilaiHuruf = 'E';
    }
}

int main() {
    const int MAX_STUDENTS = 100;
    Student students[MAX_STUDENTS];
    int n;

    cout << "Enter the number of students (max 100): ";
    cin >> n;

    if (n > MAX_STUDENTS) {
        cout << "The maximum number of students is 100." << endl;
        return 1;
    }

    for (int i = 0; i < n; ++i) {
        cout << "\nEnter data for student " << i + 1 << ":" << endl;
        cout << "NPM: ";
        cin >> students[i].npm;
        cin.ignore(); // to ignore newline character after integer input
        cout << "Name: ";
        getline(cin, students[i].name);
        cout << "Nilai UTS: ";
        cin >> students[i].nilaiUts;
        cout << "Nilai Semester: ";
        cin >> students[i].nilaiSemester;

        calculateFinalScore(students[i]);
    }

    cout << "\nStudent Data and Final Grades:\n";
    cout << "NPM\tName\t\tNilai UTS\tNilai Semester\tNilai Akhir\tNilai Huruf\n";
    for (int i = 0; i < n; ++i) {
        cout << students[i].npm << "\t" << students[i].name << "\t\t" 
             << students[i].nilaiUts << "\t\t" << students[i].nilaiSemester << "\t\t" 
             << students[i].nilaiAkhir << "\t\t" << students[i].nilaiHuruf << endl;
    }

    return 0;
}
