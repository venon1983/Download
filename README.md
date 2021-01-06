Download

<h4>Build 33</h4>
- oprava prace s kruhovym bufferm kdyz se zprava rozdely na vice casti

<h4>Build 34</h4>
- pozicovani CU_Payload_Length

<h4>Build 35</h4>
<h5>ESP</h5>
- navýšeni stacku pro websocket z 2000 -> 4000
- oprava zobrazeni baterie pro monitor
<h5>STM</h5>
- pridane vypisy

<h4>Build 36</h4>
<h5>ESP</h5>
- oprava RX bufferu
- posilani signalu
<h5>STM</h5>
- oprava RX bufferu
- posilani signalu

<h4>Build 37</h4>
<h5>ESP</h5>
- blize nespecifikovane upravy Honzi S. na reconect Wifi

<h4>Build 38</h4>
<h5>ESP</h5>
- oprava posilani Impedance, Napeti zeme, Oprava Faults
<h5>STM</h5>
- oprava posilani Impedance, Napeti zeme, Oprava Faults
- zahrnuti uprav pro advance setup

<h4>Build 39</h4>
<h5>ESP</h5>
- Novy SW pro STM
<h5>STM</h5>
- oprava bugu na silny signalu
- oprava BarLine
- oprava navratu obrazovky po remotePairing

<h4>Build 40</h4>
<h5>ESP</h5>
- predelani blokovani odesilani logu na chyby na serveru
- 20 sec timeout na blok serveru
- nova verze STM
<h5>STM</h5>
- oprava posilani stejneho PackageId
- OutOfRange je nastavovan pres = a ne pres |=
- oprava dat z energy

<h4>Build 41</h4>
<h5>ESP</h5>
- nova verze STM
*json_parser.c*

- pri eventu LOG_CREATED, Internal server error, ostatnich errorech  se posila do STM log finished cimz se odblokovava komunikace na refresh hodnot

*rs232.c*

- oprava posilani "--" na VOLTAGE_FENCE
- oprava posilani "--" na LOW_THRESHOLD
- oprava posilani "--" na SET STATE

*rs232.h*

- novy CMD ->RS232_TX_CMD_LOG_FINISHED					0x1B
*timers.c*

- pri timeoutu 20 sec na odpoved pri logu posila do STM log finished cimz se odblokovava komunikace na refresh hodnot

<h5>STM</h5>

*json_parser.c*

- pri eventu LOG_CREATED, Internal server error, ostatnich errorech  se posila do STM log finished cimz se odblokovava komunikace na refresh hodnot

*rs232.c*

- oprava posilani "--" na VOLTAGE_FENCE
- oprava posilani "--" na LOW_THRESHOLD
- oprava posilani "--" na SET STATE

*rs232.h*

- novy CMD ->RS232_TX_CMD_LOG_FINISHED					0x1B

*timers.c*

- pri timeoutu 20 sec na odpoved pri logu posila do STM log finished cimz se odblokovava komunikace na refresh hodnot

<h4>Build 42</h4>
<h5>ESP</h5>
<h5>STM</h5>

<i><b>Cloud_Uart</i></b>

- pokud se resetuje ESP behem vybirani quelle -> Neodesle se nic a na RTT se vypise log
- pridavani zprav do RTT -> CMD_END_CONFIG
- pokud je FrameCounter == 1 je na cloud posilan opakovace (jako jedinny)
- pokud CU_Payload_Length > 100 do RTT se vypise Error

<i><b>ProcessCoreTask.c</i></b>

- Pokud se odesila Our Of Range posila se s FrameCounterem = 1

<i><b>TaskCore.c</i></b>

- Out of range se posila v pripade ze zadne jine zarizeni neposila, co kazdych 15 minut

<i><b>proced.h</i></b>

- cteni HW verze desky

<i><b>main.c</i></b>

- globalni promenna HW_Version

<i><b>Update submodul SX1262 - 1.04</i></b>

- podpora noveho krystalu pro desky GAT01-RFS-08

<h4>Build 42</h4>
<h5>ESP</h5>
- novy build <b>stm 1.96</b>
<h5>STM</h5>

- oprava timeoutu nekomunikace se slavy
- pridani rolovani textu
- oprava posilani signalu
- oprava posilani impedance
- pridane posilani nazvu do radia

<h4>Build 44</h4>
<h5>ESP</h5>
- build 0.35
- bugfix memcpy zaporneho cisla

<h5>STM - ASW : build 2.00</h5>

<i><b>LCDTask</i></b>

- uprava grafiky aby se zobrazila sila prijateho testovaciho signalu

<i><b>TaskCore</i></b>

- Zakazani  generovani "nahodne" mac adresy v pripade 0 ulozene -> reseno primov bootloaderu

<i><b>TaskCloud</i></b>

- oprava pretypovani pointru (kvuli warningu)

<i><b>Cloud Uart</i></b>

- includovani watchdog controleru iwdg.h
- zapis SSID + PASSW probiha pres cyklus + obnova watchdogu
- pokud jsem na strankach QR_AP_SCEEN + QR_ADD_SCREEN a dojde k pripojeni na wifi stranka se zavre
- Odstraneni nepouzivane fce CU_Rx_CMD_Parsing

<h5>STM - BSW : build 2.16</h5>

- vypisy chyb 
- HW 0x81 - MAC 0
- HW 0x82 - MAC Spatny format
- HW 0x83 - MAC reserva
- HW 0x41 - ASW version 0
- HW 0x42 - CRC wrong
- zobrazeni MAC adresy
- zobrazeni ze se jedna o CRC skipera


<h4>Build 44</h4>

<h5>ESP</h5>

<h5>STM - ASW : build 2.01</h5>

- zapnuti WatchDogu

<h4>Build 45</h4>

<h5>ESP</h5>

<h5>STM - ASW : build 2.01</h5>

- vypnuti WatchDogu

<h4>Build 46</h4>

<h5>ESP</h5>

- pridani prepinace na devel / release sandbox

<h5>STM - ASW : build 2.10</h5>

- implementace vetve 426, 422


<h4>Build 48</h4>

<h5>ESP 38</h5>

- Pridani moznosti pripojit se k nezabezpecene wifi

<h5>STM - ASW : build 2.20</h5>

- implementace vetve 431,435,433,434











