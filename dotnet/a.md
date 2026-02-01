# .NET

## Apa itu .NET?

.NET adalah platform / ekosistem untuk membangun aplikasi. Dan .NET bukanlah bahasa pemrogramman.

## Bahasa pemrograman di .NET

1. C#
   - bahasa paling populer di .NET
   - “Java-nya .NET”
   - paling sering dipakai di ASP.NET, backend API, desktop, dll

2. F#
   - bahasa functional (mirip OCaml / Haskell style)
   - dipakai untuk data processing / finance / domain tertentu

3. VB.NET
   - Visual Basic versi .NET
   - masih ada, tapi jarang dipakai untuk project baru

> Kekeliruan umum: orang sering bilang “.NET itu C#”. Padahal C# itu bahasa, sedangkan .NET itu platform.

## Framework / Produk .NET yang sering tertukar

1. .NET Framework (lama)
   - khusus Windows
   - legacy
   - masih banyak dipakai di aplikasi kantor lama

2. .NET Core (transisi)
   - generasi baru yang cross-platform
   - dulu namanya .NET Core (v1, v2, v3)

3. .NET (modern) (sekarang)
   - sejak .NET 5, Microsoft menghapus nama “Core”
   - jadi sekarang namanya cukup .NET
   - contoh: .NET 6, .NET 7, .NET 8, .NET 10

> Kekeliruan umum: Banyak orang masih bilang “.NET Core” padahal sekarang sudah cukup “.NET”.

## Runtime: tempat program berjalan

1. CLR (Common Language Runtime)
   - runtime “klasik” untuk .NET Framework
   - menangani memory, garbage collector, exception, dll

2. CoreCLR
   - runtime modern untuk .NET Core / .NET (versi baru)
   - lebih cepat dan cross-platform

3. NET Runtime
   - istilah umum untuk runtime versi sekarang

> Analoginya: runtime itu seperti “mesin” yang menjalankan program.

## Framework untuk bikin aplikasi (jenis aplikasinya)

1. ASP.NET Core
   - untuk web backend / API
   - ini yang biasanya dipakai untuk bikin REST API seperti FastAPI di Python
   - contoh: API + JWT + Swagger

2. Blazor
   - bikin web UI pakai C#
   - ada Blazor Server & Blazor WebAssembly
   - ini semacam React/Vue tapi C#

3. MAUI (.NET MAUI)
   - bikin aplikasi mobile/desktop (Android, iOS, Windows, macOS)
   - penerus Xamarin (framework untuk membuat aplikasi mobile (Android & iOS) menggunakan C# + .NET)

4. WPF / WinForms
   - desktop Windows
   - masih populer untuk aplikasi internal perusahaan

## Compiler dan build tools

1. Roslyn
   - compiler C# modern
   - juga dipakai untuk code analysis, linting, dll

2. MSBuild
   - build engine yang dipakai Visual Studio & dotnet build

3. dotnet CLI
   - command-line tools
   - contoh:
     - dotnet new (membuat project)
     - dotnet run (menjalankan app)
     - dotnet build (Compile project)
     - dotnet test (Menjalankan unit test)

## Package manager

### NuGet

tempat install dependency/library, sama halnya seperti pip (Python)dan npm (Node)

## Assembly, DLL, EXE (sering bikin bingung)

Hasil compile C# biasanya berupa: `.dll` (library) dan `.exe` (app). Tapi di `.NET modern` kadang app juga berupa dll yang dijalankan via runtime: `dotnet app.dll`

Istilah penting:

- Assembly = unit output .NET (dll/exe)
- IL (Intermediate Language) = bytecode .NET sebelum dijalankan
- JIT (Just-in-time compilation) = compile IL ke machine code saat runtime
- AOT (Ahead-of-time) = compile jadi native lebih dulu (untuk performa/startup)

## Beberapa kekeliruan pemahaman di .NET

### .NET itu bahasa

yang benar: .NET itu platform, bahasanya C#/F#/VB.NET

### .NET Framework sama dengan .NET

yang benar:

- .NET Framework = Windows-only, legacy
- .NET (6/7/8) = modern, cross-platform

### ASP.NET itu .NET

ASP.NET itu bagian dari .NET untuk web.

ASP.NET Core = web framework di platform .NET

### .NET Core beda total dengan .NET

Sekarang:

- .NET Core sudah “melebur” jadi .NET modern.
- istilah .NET Core itu lebih ke sejarah versi 1-3.

## Perbandingan singkat .NET dan Java agar lebih faham

Mirip dari sisi konsep:

- C# ~ Java
- CLR/CoreCLR ~ JVM
- NuGet ~ Maven/Gradle
- ASP.NET Core ~ Spring Boot

Bedanya:

- .NET sangat kuat di Windows ecosystem + enterprise
- Java sangat kuat di cross-platform server ecosystem sejak dulu
