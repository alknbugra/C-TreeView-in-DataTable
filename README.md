# C-TreeView-in-DataTable

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

            https://github.com/alknbugra/C-TreeView-in-DataTable/blob/master/github1.PNG
            https://github.com/alknbugra/C-TreeView-in-DataTable/blob/master/github2.PNG
