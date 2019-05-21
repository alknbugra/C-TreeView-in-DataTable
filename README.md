# C-TreeView-in-DataTable

![github2](https://user-images.githubusercontent.com/29266933/58073301-dcc3ff80-7baa-11e9-8b4c-59e1bbf710b6.PNG)
![github1](https://user-images.githubusercontent.com/29266933/58073311-e0578680-7baa-11e9-9ea8-74e04b19dc94.PNG)

```sh

string[] dizi = { "Sipariş Seri No", "Test Hata Kayıt Detayı", " Hatalı Pozisyon", "Hata Tanımı", "Yapılan İşlem", "Tamir eden Sicil", "Tamir Tarih Saat", "Master Kod", "Test TarihSaat", "Line", "Kart Kodu", "Kart Tanımı", "Oturum", "Ürün Tanımı", "Sipariş No", "Üretim Line" };

            //*** clear
            treeView1.Nodes.Clear();
            treeView1.Font = new System.Drawing.Font("Tahoma", 12);
            
            //treeview column nodes add
            for (int i = 0; i < dizi.Length; i++)
            {
                treeView1.Nodes.Add(dizi[i].ToString());
            }
            
            //treeview node in nodes add
            for (int i = 0; i < anatable.Rows.Count; i++)
            {
                for (int k = 0; k < anatable.Columns.Count; k++)
                {
                    if (anatable.Rows[i][k].ToString() != "")
                    {
                        treeView1.Nodes[k].Nodes.Add(anatable.Rows[i][k].ToString());
                    }
                    else
                    {
                        treeView1.Nodes[k].Nodes.Add("boş");
                    }
                }
            }
                        
```
