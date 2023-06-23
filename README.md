using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace WindowsFormsApp1
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            //НачальноезначениеX
            textBox1.Text = "4";
            //НачальноезначениеY
            textBox4.Text = "2";
            //НачальноезначениеZ
            textBox3.Text = "29";
            textBox5.Text = "5";
        }

        private void button1_Click(object sender, EventArgs e)
        {
            int a = int.Parse(textBox1.Text);
            int b = int.Parse(textBox4.Text);
            int p = int.Parse(textBox3.Text);
            int g = int.Parse(textBox5.Text);
            double A = Math.Pow(g, a) % p;
            textBox2.Text += Environment.NewLine + "A = " + A.ToString();
            double B = Math.Pow(g, b) % p;
            textBox2.Text += Environment.NewLine + "B = " + B.ToString();
            double Ka = Math.Pow(B, a) % p;
            textBox2.Text += Environment.NewLine + "Ka = " + Ka.ToString();
            double Kb = Math.Pow(A, b) % p;
            textBox2.Text += Environment.NewLine + "Kb = " + Kb.ToString();
            if (Ka == Kb)
            {
                textBox2.Text += Environment.NewLine + "K = " + "Ka = " + "Kb";
            }
        }
    }
}
