# lab-assisment
#include <iostream>

int main() {
using namespace std;

void analyzeDNA(const char* dna) {
    int countA = 0, countT = 0, countC = 0, countG = 0;
    int length = strlen(dna);
    
    for (int i = 0; i < length; i++) {     
        switch (dna[i]) {
            case 'A': countA++; break;
            case 'T': countT++; break;
            case 'C': countC++; break;
            case 'G': countG++; break;
        }
    }
    cout << "A: " << countA << "\nT: " << countT << "\nC: " << countC << "\nG: " << countG << endl;

    char* rna = new char[length + 1];
    strcpy(rna, dna);
    
    for (int i = 0; i < length; i++) {
        if (rna[i] == 'T') rna[i] = 'U';
    }

    cout << "RNA Sequence: " << rna << endl;
    delete[] rna;
}
int main() {
    char dna[] = "ATGCTTAGC";
    analyzeDNA(dna);
    return 0;
