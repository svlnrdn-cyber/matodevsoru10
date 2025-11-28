<pre>
#include '<iostream>'
#include '<cmath>'

using namespace std;

// f(x) = (e^x) / (x + 1)  fonksiyonunun x = 0 noktasındaki türevi nedir?
double derivative_q10(double x)
{
    //bölümün türevi kullanılır.
    double numerator = x * exp(x);
    double denominator = pow(x + 1.0, 2.0);

    // x = -1 için tanımsızlık kontrolü
    if (denominator == 0.0)
    {
        return NAN; // Tanımsız
    }

    return numerator / denominator;
}

int main()
{
    const double X_VALUE = 0.0;

    double result_q10 = derivative_q10(X_VALUE);

    cout << "f'(x) = (x * e^x) / (x + 1)^2" << endl;
    cout <<" f'(x) değeri: 0 " << endl;

    return 0;
}
</pre>
