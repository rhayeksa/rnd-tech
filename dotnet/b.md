# Sourcode .NET

Ada beberapa perintah .NET CLI untuk memulai membuat project .NET baru. Perintah ini biasanya digunakan untuk generate struktur project secara otomatis.

Beberapa template yang paling sering digunakan:

- `dotnet new console -n <project_name>` Digunakan untuk membuat aplikasi berbasis Console / CLI.
- `dotnet new webapi -n <project_name>` Digunakan untuk membuat project ASP.NET Core Web API (backend API).
- `dotnet new mvc -n <project_name>` Digunakan untuk membuat project ASP.NET Core MVC (Fullstack server-rendered: Controller + View).
- `dotnet new classlib -n <project_name>` Digunakan untuk membuat Class Library, biasanya untuk logic yang reusable (Service, Helper, Shared Library).
- `dotnet new xunit -n <project_name>` Digunakan untuk membuat project Unit Test dengan xUnit.

Selain membuat project baru, beberapa command yang paling sering dipakai developer:

- `dotnet run`, menjalankan aplikasi
- `dotnet build`, compile/build project
- `dotnet test`, menjalankan unit test
- `dotnet add package <package_name>`, install dependency/library dari NuGet
- `dotnet restore`, download dependency sesuai file `.csproj`

## Simple Hello World Console

1. Jalankan perintah berikut untuk membuat project console:

   ```bash
   dotnet new console -n MyFirstConsoleProject
   ```

2. Masuk ke folder project:

   ```bash
   cd MyFirstConsoleProject
   ```

3. Jalankan project:

   ```bash
   dotnet run
   ```

Maka output default akan menampilkan:

```bash
Hello, World!
```

> File `Program.cs` merupakan entry point / file utama pada project Console .NET (tempat kode utama dieksekusi pertama kali).

## Simple Hello World Web API .NET (ASP.NET Core)

1. Buat Project Web API

   ```bash
   dotnet new webapi -n HelloApi
   cd HelloApi
   dotnet run
   ```

   > Defaultnya akan jalan di port misalnya: `http://localhost:5xxx`

2. Tambahkan Endpoint GET /hello

   Buka file Program.cs, lalu tambahkan endpoint code ini :

   ```c#
   // ...
   app.MapGet("/hello", (string? name) =>
   {
    if (string.IsNullOrWhiteSpace(name))
        return Results.Ok(new { message = "Hello, Stranger!" });

    return Results.Ok(new { message = $"Hello, {name}!" });
   });

   app.Run();
   ```

3. Run kembali dan coba
   - Tanpa parameter

     ```bash
     curl "http://localhost:5xxx/hello"
     ```

     Response:

     ```json
     { "message": "Hello, Stranger!" }
     ```

   - Dengan parameter

     ```bash
     curl "http://localhost:5000/hello?name=Rhayeksa"
     ```

     Response:

     ```json
     { "message": "Hello, Rhayeksa!" }
     ```
