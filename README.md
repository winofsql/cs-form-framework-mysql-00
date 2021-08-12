# cs-form-framework-mysql-00
Form で MySQL を読み出して TextBox にセットしてから Debug.WriteLine で表示
```cs
myReader = myCommand.ExecuteReader();

// myReader からデータが読みだされる
if (myReader.Read())
{
    // 列名より列番号を取得
    int index = myReader.GetOrdinal("氏名");
    // 列番号で、値を取得して文字列化
    string text = myReader.GetValue(index).ToString();
    // 出力ウインドウに出力
    Debug.WriteLine($"Debug:{text}");

    this.textBox1.Text = text;
}
```
