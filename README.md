# datatable
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Latihan 1</title>
    <style>
        #simpan{
            padding: 10px; 
            width:100%; 
            background-color: yellow;
            border-radius: 10px;
            color:black;
            border-width: 1px;
        }
        #simpan:hover{
            color:blanchedalmond;
            background-color: black;
        }
    </style>
    <link rel="stylesheet" href="DataTables/datatables.min.css">
</head>
<body>
    <table style="font-family: 5px;" width="50%" align="center">
        <tr>
            <td colspan="8" align="center"><h3>Input Data Ke Tabel</h3></td>
        </tr>
        <tr>
            <td>Nama</td>
            <td><input style="width: 90%; padding: 5px;border-radius: 10px;"type="text" name="nama" placeholder="Masukan Nama" /></td>
            <td>Kelas</td>
            <td><input style="width: 90%; padding: 5px;border-radius: 10px;"type="text" name="kelas" placeholder="Masukan Kelas" /></td>
        </tr>
        <tr>
            <td>Alamat</td>
            <td>
                <input style="width: 90%; padding: 5px;border-radius: 10px;"type="text" name="alamat" placeholder="Masukan Alamat" /></td>
                <td>No Hp</td>
                <td><input style="width: 90%; padding: 5px;border-radius: 10px;"type="text" name="hp" placeholder="Masukan No Hp" /></td>
        </tr>
        <tr>
            <td colspan="8" align="center">
                <button id="simpan">Simpan Data</button>

            </td>
        </tr>
    </table>

    <table id="table" class="table">
        <thead>
            <tr>
                <th width="10%">No</th>
                <th width="25%">Nama</th>
                <th width="10%">Kelas</th>
                <th width="5%">Alamat</th>
                <th width="5%">No HP</th>
            </tr>
        </thead>
    </table>
    <script src="DataTables/jQuery-3.6.0/jQuery-3.6.0.min.js"></script>
    <script src="DataTables/datatables.min.js"></script>
    <script>
        
        
            // var data = [["1","Kim Rio","XII RPL 2","Jalan Jalan","08357465437"]];
            var tabel = $("#table").DataTable({
            responsive : true,
            // data : data
        });
        tabel.on('click','tr',)
        var no = 1;
            $("#simpan").click(function(){
            var nama = $("input[name=nama]").val();
            var kelas = $("input[name=kelas]").val();
            var alamat = $("input[name=alamat]").val();
            var hp = $("input[name=hp]").val();
            
            tabel.row.add(
                [ no,nama,kelas,alamat,hp]
            ).draw(false);
            
            no++;
        //     console.log(nama);
        //     console.log(kelas);
        //     console.log(alamat);
        //     console.log(hp);
         });
       
        //     var data = [];
        //     for (let i = 0; i < 5; i++) {
        //         data.push([i]);
        //     for (let j = 0; j < 5; j++) {
        //         data[i].push(j);
        //     }
        // }
      
    </script>
</body>
</html>
