# poker_csharp
practice csharp

名稱：撲克牌比大小

功能：

1.按 開始 啟動計時器，計時器會以每0.05秒用亂數切換poker1.jpg~poker13.jpg 撲克牌圖。

2.按 暫停 顯示點數及對應鋪克牌圖。



![poker](https://github.com/user-attachments/assets/4d854344-3156-4d19-be26-441e6d250540)



 using System.Diagnostics.Eventing.Reader;

namespace G
{
    public partial class Form1 : Form
    {
        int point;
        int pointpc;
        Random rand = new Random();
        public Form1()
        {
            InitializeComponent();
        }

        private void label1_Click(object sender, EventArgs e)
        {

        }

        private void Form1_Load(object sender, EventArgs e)
        {
            label3.Text = "";
            timer1.Interval = 100;
            pictureBox1.SizeMode = PictureBoxSizeMode.StretchImage;
            pictureBox2.SizeMode = PictureBoxSizeMode.StretchImage;

        }

        private void button1_Click(object sender, EventArgs e)
        {
            timer1.Start();
            pointpc = rand.Next(13);
        }

        private void button2_Click(object sender, EventArgs e)
        {
            timer1.Stop();
            if (point > pointpc)
            {
                label4.Text = " You Win!";
            }
            else if (point < pointpc)          
            {
                label4.Text = "computer win!";
            }
            else
            {
                label4.Text = "Drow";
            }
        }

        private void timer1_Tick(object sender, EventArgs e)
        {
            point = rand.Next(13);
            pictureBox2.Image = imageList1.Images[point];
            pictureBox1.Image = imageList1.Images[pointpc];
        }

        private void pictureBox2_Click(object sender, EventArgs e)
        {

        }

        private void pictureBox1_Click(object sender, EventArgs e)
        {
        }
    }
}
        private void pictureBox1_Click(object sender, EventArgs e)
        {
        }
    }
}
