# ProjetoFormsMedia
CRIE UM PROJETO WINDOWS FORMS CHAMADO "PROJETOFORMSMEDIA" E TENHA 4 TEXTBOX´S PARA RECEBER AS NOTAS PARA O CÁLCULO DA MÉDIA ARITMÉTICA.

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace ProjetoFormsMedia1
{
public partial class Form1 : Form
{
public Form1()
{
InitializeComponent();
}
decimal Nota1, Nota2, Nota3, Nota4, Media;

private void txtNota1_TextChanged(object sender, EventArgs e)
{

}

private void label2_Click(object sender, EventArgs e)
{

}

private void txtNota2_TextChanged(object sender, EventArgs e)
{

}

private void label3_Click(object sender, EventArgs e)
{

}

private void txtNota3_TextChanged(object sender, EventArgs e)
{

}

private void label4_Click(object sender, EventArgs e)
{

}

private void txtNota4_TextChanged(object sender, EventArgs e)
{

}

private void lblStatus_Click(object sender, EventArgs e)
{

}

private void label1_Click(object sender, EventArgs e)
{

}

private void btnLimpar_Click(object sender, EventArgs e)
{
txtNota1.Clear();
txtNota2.Clear();
txtNota3.Clear();
txtNota4.Clear();
lblStatus.Text = "";
lblResultado.Text = "";
txtNota1.Focus();
}

private void lblResultado_Click(object sender, EventArgs e)
{
if (Media >= 7)
{
lblResultado.Text = lblResultado.ToString();
lblResultado.Text = ("Aprovado"); 
}
else if (Media >= 5 && Media < 7)
{
lblResultado.Text = lblResultado.ToString();
lblResultado.Text = ("Recuperação");
}
else if (Media < 5)
{
lblResultado.Text = lblResultado.ToString();
lblResultado.Text = ("Reprovado");
}
}

private void btnMedia_Click(object sender, EventArgs e)
{
if (txtNota1.Text == "" || txtNota2.Text == "" || txtNota3.Text == "" || txtNota4.Text == "")
{
lblStatus.Text = "Preencha os campos!";
}
else
{
lblStatus.Text = "";
Nota1 = Convert.ToDecimal(txtNota1.Text);
Nota2 = Convert.ToDecimal(txtNota2.Text);
Nota3 = Convert.ToDecimal(txtNota3.Text);
Nota4 = Convert.ToDecimal(txtNota4.Text);
Media = (Nota1 + Nota2 + Nota3 + Nota4) / 4;
}

}
}
}
