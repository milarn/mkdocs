# Autopilot HWID

## Enkel metode:
i cmd på en nytanket maskin trykk shift + f10 for å få opp cmd ved tastatur-valg. 
i cmd skriv:
`C:\Users\bruker>powershell.exe`
Etter dette er gjort er powershell aktivert og du kan nå fortsette med å skrive inn:

`Set-ExecutionPolicy -Scope Process -ExecutionPolicy Unrestricted`

`Install-Script -Name Get-WindowsAutoPilotInfo`
Når du installerer Get-WindowsAutoPilotInfo så får du en del valg du må godta ved å skrive `Y` eller `A` Husk at dette også krever nett-tilgang.

For å aktivere skriptet skriv:

`Get-WindowsAutoPilotInfo.ps1 -Online`

Her kommer det opp et vindu med autentisering til din Tenant. Husk at brukeren som melder disse maskinene inn må ha AAD rollen: `Intune administrator`



Skript for å hente ut maskinvare hash fra eksiterende PC som vi eier med powerhell
 
Set-Location -Path "D:\HWID"
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Unrestricted
Install-Script -Name Get-WindowsAutoPilotInfo
Get-WindowsAutoPilotInfo.ps1 -OutputFile AutoPilotHWID.csv
 
Powershellskript kjøres som administrator. PC må være koblet til internett for at dette skal virke. 
Svar ja på all godkjenning som dukker opp.
 
Outputfilen blir lagret på minnepenn: D:\HWID\  - Outputfilen heter her AutoPilotHWID.csv
Derfor er det viktig å ha denne mappen på minnepenn klar. HWID mappen er opprettet på forhånd.
