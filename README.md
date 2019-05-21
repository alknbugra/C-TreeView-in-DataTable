# C-TreeView-in-DataTable

```sh
            treeView1.Nodes.Clear();
            treeView1.Font = new System.Drawing.Font("Tahoma", 12);
            for (int i = 0; i < dizi.Length; i++)
            {
                treeView1.Nodes.Add(dizi[i].ToString());
            }
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
