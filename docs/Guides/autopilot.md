# Autopilot HWID

## Enkel metode:
i cmd på en nytanket maskin trykk shift + f10 for å få opp cmd ved tastatur-valg. 
i cmd skriv:
`C:\Users\bruker>powershell.exe`
Etter dette er gjort er powershell aktivert og du kan nå fortsette med å skrive inn:

`PS C:\Users\bruker>Set-ExecutionPolicy -Scope Process -ExecutionPolicy Unrestricted`

`PS C:\Users\bruker>Install-Script -Name Get-WindowsAutoPilotInfo`
Når du installerer Get-WindowsAutoPilotInfo så får du en del valg du må godta ved å skrive `Y` eller `A` Husk at dette også krever nett-tilgang.

For å aktivere skriptet skriv:

`PS C:\Users\bruker>Get-WindowsAutoPilotInfo.ps1 -Online`

Her kommer det opp et vindu med autentisering til din Tenant. Husk at brukeren som melder disse maskinene inn må ha AAD rollen: `Intune administrator`



## Skript for å hente ut maskinvare hash fra eksiterende PC som vi eier med powerhell

Her er det litt det samme, bare at vi trenger en usb for å få ut HWID. På USB-en lager du en mappe som heter HWID.

Set-Location -Path "D:\HWID"
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Unrestricted
Install-Script -Name Get-WindowsAutoPilotInfo
Get-WindowsAutoPilotInfo.ps1 -OutputFile AutoPilotHWID.csv

Istedet for `-online` som vi brukte på den lette måten, så bruker vi `-OutputFile AutoPilotHWID.csv` her.
 
Powershellskript kjøres som administrator. PC må være koblet til internett for at dette skal virke. 
Svar ja på all godkjenning som dukker opp.
 
Outputfilen blir lagret på minnepenn: D:\HWID\  - Outputfilen heter her AutoPilotHWID.csv
Derfor er det viktig å ha denne mappen på minnepenn klar.

 ![auto1](\img\autopilot1.png)

 ![auto2](\img\autopilot2.png)

Etter dette må vi inn på endpoint.microsoft.com og laste denne filen opp.

 ![auto4](\img\autopilot4.png)
 
 ![auto5](\img\autopilot5.png)