using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;

namespace WpfApplication10
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
        }

        private void button_Click(object sender, RoutedEventArgs e)
        {

            listBox.Items.Clear();
            int[] lottery_numbers = new int[5];
            
            for (int i = 1; i != lottery_numbers.Length; i++) {
                lottery_numbers[i] = i;
                listBox.Items.Add(lottery_numbers[i]);
            }
        }

        private void button1_Click(object sender, RoutedEventArgs e)
        {
            listBox.Items.Clear();
            int specify_number;
            specify_number = int.Parse(textBox.Text);
            int[] lottery_numbers = new int[specify_number];

            for (int i = 0; i != lottery_numbers.Length; i++)
            {
                lottery_numbers[i] = i + 1;
                listBox.Items.Add(lottery_numbers[i]);
            }
        }

        private void btn_excersice_Click(object sender, RoutedEventArgs e)
        {
            listBox.Items.Clear();
            int multiply_number;
            multiply_number = int.Parse(textBox.Text);
            int[] lottery_umbers = new int[multiply_number];
            for (int i=0; i!=lottery_umbers.Length; i++)
            {
                lottery_umbers[i] = multiply_number * i;
                listBox.Items.Add(multiply_number + "times"+ i + "=" + lottery_umbers[i]);
            }
            
        }

        private void btn_dimension_Click(object sender, RoutedEventArgs e)
        {
            listBox.Items.Clear();
            int arrayrows;
            int arrayccols;

            int[,] arraytimes = new int[arrayrows, arrayccols];
            int mult=0;

            for (int i=0; i!=arrayrows; i++)
            {
                mult = mult + 10;
                for (int j=0; j!=arrayccols; j++)
                {
                    arraytimes[i, j] = mult;
                    mult = mult * 10;

                }
                mult = mult / 1000;

            }

        }
    }
}
