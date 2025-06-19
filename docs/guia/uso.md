# Cálculos Astronómicos Básicos

=== "Python"

    ```python
    def gravedad(m1, m2, r):
        G = 6.674e-11  # Constante de gravitación
        return G * (m1 * m2) / (r ** 2)
    
    fuerza = gravedad(5.97e24, 7.35e22, 384400000)
    print(f"{fuerza:.2e} N")
    ```

=== "C++"

    ```cpp
    #include <iostream>
    using namespace std;

    int main() {
        double G = 6.674e-11;
        double m1 = 5.97e24, m2 = 7.35e22, r = 384400000;
        double fuerza = G * (m1 * m2) / (r * r);
        cout << fuerza << " N" << endl;
        return 0;
    }
    ```
