# Ejercicio1
Mediante uso de GOTO en visual basic, realice el ordenamiento de 3 números.


Public Class Ordenar

    Private Sub Button1_Click(sender As Object, e As EventArgs) Handles Button1.Click
        Dim a, b, c As Integer
        a = Convert.ToInt32(TextBox1.Text)
        b = Convert.ToInt32(TextBox2.Text)
        c = Convert.ToInt32(TextBox3.Text)
        
        If a < b And a < c Then GoTo a_menor Else 
        If b < a And b < c Then GoTo b_menor Else GoTo c_menor
a_menor:
        TextBox4.Text = a
        TextBox9.Text = a
        GoTo medio
b_menor:
        TextBox4.Text = b
        TextBox9.Text = b
        GoTo medio
c_menor:
        TextBox4.Text = c
        TextBox9.Text = c
        GoTo medio
medio:
        If (a > b And a < c) Or (a > c And a < b) Then GoTo a_medio Else 
        If (b > a And b < c) Or (b > c And b < a) Then GoTo b_medio Else GoTo c_medio
a_medio:
        TextBox5.Text = a
        TextBox8.Text = a
        GoTo mayor
b_medio:
        TextBox5.Text = b
        TextBox8.Text = b
        GoTo mayor
c_medio:
        TextBox5.Text = c
        TextBox8.Text = c
        GoTo mayor
mayor:
        If a > b And a > c Then GoTo a_mayor Else 
        If b > a And b > c Then GoTo b_mayor Else GoTo c_mayor
a_mayor:
        TextBox6.Text = a
        TextBox7.Text = a
        GoTo final
b_mayor:
        TextBox6.Text = b
        TextBox7.Text = b
        GoTo final
c_mayor:
        TextBox6.Text = c
        TextBox7.Text = c
        GoTo final       
final:
        
    End Sub
