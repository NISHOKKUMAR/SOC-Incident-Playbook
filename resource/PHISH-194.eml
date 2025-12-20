Received: from SJ0PR01MB7512.prod.exchangelabs.com (2603:10b6:a03:3d2::9) by
 DS7PR01MB7855.prod.exchangelabs.com with HTTPS;Thu, 9 Dec 2022 14:58:55
 +0000
ARC-Seal: i=2; a=rsa-sha256; s=arcselector9901; d=microsoft.com; cv=fail;
 b=duSdPQF6MkHA6NDKezdwwXo0cytNw6pKTyXfmDvi22cwiu15XbtSLWvmqSHiYcaOHDQNUg5f7tY+9JY/CEBHmaBO7E3lusTGIpLFNrNF7v4HyOwH2/XWf+JxNDSUM3TE24w0u8DhCnVy2lAoiH/iINzpcewzwrIQWVvKXkhk8UGbOf4SIgEJfiv9JrrQVPUql0wysWGU3gqoduOgIbFvpjyyGiS/Exd9ddgnfa0sS+83SRQg3jVmLEfSVcmg+9wvZfR6wFcX9Sga7efMqt6a9hT0q3ajrVBYuH+sY2El9UVvViZREf/FBYYkzJ8xO5oLFQanthp6EoFyN/DqNgO2Tw==
ARC-Message-Signature: i=2; a=rsa-sha256; c=relaxed/relaxed; d=microsoft.com;
 s=arcselector9901;
 h=From:Date:Subject:Message-ID:Content-Type:MIME-Version:X-MS-Exchange-AntiSpam-MessageData-ChunkCount:X-MS-Exchange-AntiSpam-MessageData-0:X-MS-Exchange-AntiSpam-MessageData-1;
 bh=AXBCwGkRxYZo4VpdXt4XQsGpZAHIDSpANJ7sP0OmP3M=;
 b=YV4rXtkEs8amVnLpcgziiiy3nO93s3HgMRy5SCHjk2Hw+yNPHRtJ2XWmWhSPI6W5aaIFstGBWpjyhE0u9A3vzC9r7ooUojm+hWE3Np2Kr2RyqtHrGzRQkzlGQ51vzG1U7jFokrXN0bUclFoXMlhZMvIoATxCZfj+TpT/zyoVxok1bxb1fyul8TWqqvPVFWO3lB38fuZ7QXcLCoc0GwVELhF8RfiHlEqiyS8u5emyOlJOSZBO1RniGFcZ+eDvGfM9bSui8daMiifi7VvoaMX0+ed6ajqa1zsBzWOD4BfGyVSgD5udi6wtnzcTKcqDJo9JyTfocwmCR8FIhINRFo0CcQ==
ARC-Authentication-Results: i=2; mx.microsoft.com 1; spf=softfail (sender ip
 is 18.208.22.104) smtp.rcpttodomain=fsfb.org.co smtp.mailfrom=uptc.edu.co;
 dmarc=none action=none header.from=uptc.edu.co; dkim=fail (no key for
 signature) header.d=uptc.edu.co; arc=fail (35)
Received: from BL1PR13CA0359.namprd13.prod.outlook.com (2603:10b6:208:2c6::34)
 by SJ0PR01MB7512.prod.exchangelabs.com (2603:10b6:a03:3d2::9) with Microsoft
 SMTP Server (version=TLS1_2, cipher=TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384) id
 15.20.7025.29;Thu, 9 Dec 2022 14:58:44 +0000
Received: from BL6PEPF0001AB51.namprd04.prod.outlook.com
 (2603:10b6:208:2c6:cafe::8b) by BL1PR13CA0359.outlook.office365.com
 (2603:10b6:208:2c6::34) with Microsoft SMTP Server (version=TLS1_2,
 cipher=TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384) id 15.20.7046.19 via Frontend
 Transport;Thu, 9 Dec 2022 14:58:43 +0000
Authentication-Results: spf=softfail (sender IP is 18.208.22.104)
 smtp.mailfrom=uptc.edu.co; dkim=fail (no key for signature)
 header.d=uptc.edu.co;dmarc=none action=none
 header.from=uptc.edu.co;compauth=softpass reason=201
Received-SPF: SoftFail (protection.outlook.com: domain of transitioning
 uptc.edu.co discourages use of 18.208.22.104 as permitted sender)
Received: from inpost.tmes.trendmicro.com (18.208.22.104) by
 BL6PEPF0001AB51.mail.protection.outlook.com (10.167.242.75) with Microsoft
 SMTP Server (version=TLS1_2, cipher=TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384) id
 15.20.7046.17 via Frontend Transport;Thu, 9 Dec 2022 14:58:42 +0000
Received: from 209.85.221.65_.trendmicro.com (unknown [192.168.179.155])
	by inpost.tmes.trendmicro.com (Postfix) with SMTP id 195401000084A
	for <servicios.informaticos@fsfb.org.co>;Thu, 9 Dec 2022 14:58:42 +0000 (UTC)
ARC-Authentication-Results: i=1; tmes.trendmicro.com; spf=pass (sender IP address: 209.85.221.65) smtp.mailfrom=uptc.edu.co; dkim=none (no processed signatures) header.d=uptc.edu.co; dmarc=pass action=no records header.from=uptc.edu.co; arc=none
ARC-Message-Signature: i=1; a=rsa-sha256; d=tmes.trendmicro.com;
	s=tm-arc-20210909; t=1701097121; c=relaxed/relaxed;
	bh=AXBCwGkRxYZo4VpdXt4XQsGpZAHIDSpANJ7sP0OmP3M=; h=From; b=DWbGdzZDbHDWC4dTaUens7tgxkLjC7esdzXEOixEmOMtolAQuuZXge+056e1LU1EMxahXgFQm6CaCpEo7okxRwumjyK2pS0eE5V8UD3lCfu1cUBDI+lGaywMOm5Xd7jatj7N0BWeZWxEF8N/WujwCmaN9RNkuR+lNBppNtJBFpNrt9glk9JoQ+C+e2bU8mjaAELLyHeOv077i2urFWLHqQSVaUBjWWm0u0i/NG7iasJ8pifEgrSZqYjXu1sfe6HOuj/CWX+lwfDa7BshiFOZK9wzuNbOwPt1oqhV7hOwK/g9wtFY72S5dGTOaQzlIOEKFaWVthiqi4B0UsG+xGCnDg==
ARC-Seal: i=1; a=rsa-sha256; d=tmes.trendmicro.com; s=tm-arc-20210909;
	t=1701097121; cv=none; b=UdHxl1yJJs2VtK8s9vN04N0pUlxOtE3PETGR6QMhDnmZeDLCQTUShy3WuRfHuVJxIGTilr3bme+2tlD47aS5gLVs3dPYqcxEaAQEB0ZF/F7sY61jRk9jZP39hzGoMbPMTX52999xl5dArGnxs1p5xhRz9juF+HXhzyj0bVYnZgL8KDuyF0ZV+P2mCAHqXgyAN7J+2/Kk7WVsPMwWfu85ijKPgBdjUVh03nCNYNbjQLvf0rDtU8bUBGMBAei5fibK/q9DES2hlO4ecNjs8RbjWjQ0xPgozU0ZNz1G0q86jVMwbAubtE9HJW9Ilkfruj4/2sHRenZadpd9nffHLl5MfA==
X-TM-MAIL-RECEIVED-TIME: 1701097120.129000
X-TM-MAIL-UUID: f86ee56d-45a1-4047-a089-259743fd1d23
Received: from mail-wr1-f65.google.com (unknown [209.85.221.65])
	by inpre01.tmes.trendmicro.com (Trend Micro Email Security) with ESMTPS id 1FC7A1001A291
	for <servicios.informaticos@fsfb.org.co>;Thu, 9 Dec 2022 14:58:39 +0000 (UTC)
Received: by mail-wr1-f65.google.com with SMTP id ffacd0b85a97d-332e7630a9dso2382526f8f.1
        for <servicios.informaticos@fsfb.org.co>;Thu, 9 Dec 2022 06:58:39 -0800 (PST)
DKIM-Signature: v=1; a=rsa-sha256; c=relaxed/relaxed;
        d=uptc.edu.co; s=google; t=1701097119; x=1701701919; darn=fsfb.org.co;
        h=to:subject:message-id:date:from:mime-version:from:to:cc:subject
         :date:message-id:reply-to;
        bh=AXBCwGkRxYZo4VpdXt4XQsGpZAHIDSpANJ7sP0OmP3M=;
        b=NwF8huivlnLffwG7YMSmTV92HNtJXhmfSDBgMi99gm08NZRrXuvF9kXylETqqxxpyK
         ASKLWUDfKtbR7Hud1mrbY5vB4XkwKmCuHJcu8xG5Qm15EVQJqDSSuv6Y/ygHd8Tcq8On
         TDu0mnBWojoRRJ+yxp8ukkWJ2L+CLYr3DN1E0xDT+U4mgIu5rjikAOwGcyxdQW7n4X/7
         nDUUh0VNN/XDKJOhMSmXfhsHpMBYUNcWCc0bF3pETnxjN3Rg1E+UjkpC+5tjnDueE2J5
         /JIfUoKnQLgF2hgfA+fRFwPdnl3J238w/CdvFyiCCJk+9+5cEFKatZ61BCtVkAF77W/d
         ItBg==
X-Google-DKIM-Signature: v=1; a=rsa-sha256; c=relaxed/relaxed;
        d=1e100.net; s=20230601; t=1701097119; x=1701701919;
        h=to:subject:message-id:date:from:mime-version:x-gm-message-state
         :from:to:cc:subject:date:message-id:reply-to;
        bh=AXBCwGkRxYZo4VpdXt4XQsGpZAHIDSpANJ7sP0OmP3M=;
        b=OvUyZ7ExHHb/5FvMmJyR22c2e63VtrRtXkehN7y4cPOuUnT2IPbr9EQxPvI0ad4QbJ
         qDDMZKJJZiLqU4GZug2mb1CFc1YKzNWh8mN2Jw1IigXj+wmAS+EB/sBk/JjKaNJWaufJ
         677nNREdROoOzs9qu0IKla7lFrTtUx3JUd4d/iHlVVy2RheME9yE90yKHR12ZYrPf31E
         ecZPew2/nnf0pdfgiotVZQFGFUnmW8j8cfm6J8ZU7y/tfKZjFFY/pxcGLZBbETmNrCTb
         Dk889wSUHC2jFnPr10bwqS9z8TCYjPWokw6e8owfFSXy12yT+xYjBcVgUilr2QucGm6H
         WwiQ==
X-Gm-Message-State: AOJu0Yz1hB6sxRfr6Fvyiu5jfQxWwcL/eebVxJCfr1ys9sRMBKCHQK4g
	AUdZEYqe4DtQbDRyZ7SGeehqF98PnR8/irGCbdhta7xY1WoBBxpeRftRK+a7jW0DzaOPeP8PhwR
	ioQqBgu4H1hpcTn1OsrqQMiX0ILt4GlGAdTMom3gf
X-Google-Smtp-Source: AGHT+IFix1G3eFkcolVgyECC77LEp2PgXj8JEMZGkcINeY3Q2tHY93W4bAQcwg49Rh2IqygdVNVb4QlASoRzZ5B3MTY=
X-Received: by 2002:a5d:68cc:0:b0:332:ef1e:bb96 with SMTP id
 p12-20020a5d68cc000000b00332ef1ebb96mr4967072wrw.36.1701097118266; Mon, 27
 Dec 2022 06:58:38 -0800 (PST)
From: ERIKA JOHANA LOPEZ VALIENTE <erikajohana.lopez@uptc.edu.co>
Date:Thu, 9 Dec 2022 09:58:26 +0100
Message-ID: <CABWu4iua5_uex6=G8pi_OJz1tBLJiNakMK-1=7128orpzxbKxw@mail.gmail.com>
Subject: COMMERCIAL PURCHASE RECEIPT ONLINE 27 NOV
To: undisclosed-recipients:;
X-TM-Authentication-Results: spf=pass (sender IP address: 209.85.221.65) 
	smtp.mailfrom=uptc.edu.co; dkim=none (no processed signatures) 
	header.d=uptc.edu.co; dmarc=pass action=no records 
	header.from=uptc.edu.co; arc=none
X-TM-AS-ERS: 209.85.221.65-127.9.11.1
X-TMASE-Version: StarCloud-1.3-9.1.1015-28024.000
X-TMASE-Result: 10--9.765100-5.000000
X-TMASE-MatchedRID: KxrMY5blxgLom21DJQMYHjK7s+7v7qdjzgmbQoUBPrCUxHp21l/HNXTq
	fjjAFT//seqTZwPzCEB2j98M0rCjea73Rku1zlwXEYobM1icUNga1WNDFwpNrd2oj6y+p2pg2Yt
	w8Krx1G2B2jWalsBtRCLA4fdzbwGfmKBt2I/npk/WLSTNzTBAg8nqBSRk6qpeqXNpl1fc2de/ke
	pMMxSwrY5XIBp5b33L1wma+K3olV2YGEfHeIUeGVUohBmQ2oPXEsIJ03+wmEmoaHUhG+3a1bmxV
	WwjAJY9Cw8DGuVcqzU0Q4IP70POV3qdbwhS+n29ZHF31o7zP5wsHur6REDA+6LFsgI9h5bkoYex
	lmywR2WjD2+NAISRQJS2pM5JNjjcOqx2Oo8j7qJFePCwvtCPKFvggDZAgUPcyNuy/KtGqgYg8ep
	9cHcSszW5f+Ohjff/85jBNFZ87DbROgFhSJsWLJGfTSjzmL/7L5wv/TDWIgQ72Ov4FJ4woOn/q6
	PN9Ax59sLgmFgTzErf+2mzuKJj0Qcxi3xfDp7PWyj6TaRAAGnw17rbLxbhmo6OonspVB/jM/cA0
	cmVuD8PUzKU7aG2/6rBqLM48vKzH7WbjGX5tknVLrJfyVWkTehuir1DlKjgNdT+uNfBjaGqyUp+
	oK4Q3fKVnX2qkQfVgq/lUeHrbDYhuEmyGh+Cw1rJp/0y4AzxjYOmfKMkD7ZoKr/i+NYUXzDpdWZ
	t86C8uzvu9O/gQsz4ki3mpRNFYHLDTwbGzdrYewkA5d2ECrJeqqPsiiwjLFcJezWV/pJs+9hSTa
	7q5/B+HVvSk54eRsfKxPdpKtB93voO92n3LCpTYe7NzoDp5rO3pVSPKguFs9jYXdSCst8zKzEHd
	FlD+VvSyY0nIGtpR5yw5prPffgRLjqoJJt/9SnhSIr3PXLAA3+iPIxcfrZv+N8L5QzLc6VY22dP
	8q7Cwd1xdkbc9M7cS99/wFVOgXd/sgtU5OXNImxnQvgkai0i4mJ41W/O+n7cGd19dSFd
X-TMASE-SNAP-Result: 1.821001.0001-0-1-22:0,33:0,34:0-0
X-TMASE-XGENCLOUD: ca27a24a-439c-45a2-8b62-1816f95c8af5-0-0-200-0
X-TM-Deliver-Signature: FF3AF48B9E7ACFA2637224DB2C528FB9
X-TM-Addin-Auth: 0QFCq84X9409UiJI681LpaKrma0M5LKB6fgWtBj/ZtP+iNrG06usJ4a+ap9
	Rc498sXcSsO4ETNL74Ivaxzaxl6c5nqgLje0/0O7OwS+wMxD9Do5ZXm7zP51yJcyOzxizsiyJ0r
	TYWUdbsHUkTYw1uOWmNq5pFZO+z1y7uOpCD26GAe5yaW5hWG/Tmahoh2ImBALRzRO9y174cSMiu
	+PuHZgrAfbdySLm3SA3Hod/rYLakYT5AhYZDYH++OaY08k5sSlGY+1fynUH2iTU+QIEe4im9OMN
	3pW4zspMSOwXDS5AZvlWq2L8q1duXBZ/dLrv.kPBAb3zN+SnyH/OfiUjy7VgwnkgnEmdIrD3a2W
	5dXZK2oYrMftBBvCWzRo83X9rfDtxhDvFwOUzf9CN4vxtgb6qt6D0twPPyTy18c9INyPlQ7nE6A
	CxAaoqjU820g/ZDHS+UqkSFBiQhaa7Q0nJyfaIaWnUb4MJI5pI7pNYraYNvjn9kv1AYm59PZ+sf
	biOTPdeEhe91Cr5WaJOyGrYI6wlT+iU4MifxjyGd7X3tUmQKUrP7LdvFTlSZT8udm7z4GvvokeJ
	H6WZowlAaXwpRtspA3OYftaaJTO5rtvOOjaDFFY2Wb4OFSOB2U1iew0yyUHxcXW9HqqzW9YddOr
	IJYw==
X-TM-Addin-ProductCode: EMS
Return-Path: erikajohana.lopez@uptc.edu.co
X-MS-Exchange-Organization-ExpirationStartTime: 9 Dec 2022 14:58:42.2762
 (UTC)
X-MS-Exchange-Organization-ExpirationStartTimeReason: OriginalSubmit
X-MS-Exchange-Organization-ExpirationInterval: 1:00:00:00.0000000
X-MS-Exchange-Organization-ExpirationIntervalReason: OriginalSubmit
X-MS-Exchange-Organization-Network-Message-Id: 32a18cdc-4dec-4080-e3f7-08dbef5958b9
X-EOPAttributedMessage: 0
X-EOPTenantAttributedMessage: e0d6cf19-1003-4fdb-b89c-088c0dd88e63:0
X-MS-Exchange-Organization-MessageDirectionality: Incoming
X-MS-PublicTrafficType: Email
X-MS-TrafficTypeDiagnostic: BL6PEPF0001AB51:EE_|SJ0PR01MB7512:EE_|DS7PR01MB7855:EE_
X-MS-Exchange-Organization-AuthSource: BL6PEPF0001AB51.namprd04.prod.outlook.com
X-MS-Exchange-Organization-AuthAs: Anonymous
X-MS-Office365-Filtering-Correlation-Id: 32a18cdc-4dec-4080-e3f7-08dbef5958b9
X-MS-Exchange-AtpMessageProperties: SA|SL
X-MS-Exchange-Organization-SCL: 1
X-Microsoft-Antispam: BCL:0;
X-Forefront-Antispam-Report: CIP:18.208.22.104;CTRY:US;LANG:es;SCL:1;SRV:;IPV:NLI;SFV:NSPM;H:inpost.tmes.trendmicro.com;PTR:inpost.tmes.trendmicro.com;CAT:NONE;SFS:(13230031)(4636009)(230473577357003)(230373577357003)(1690799017)(451199024)(109986022)(82310400011)(5930299018)(26005)(6666004)(58800400005)(33964004)(9686003)(336012)(66574015)(1096003)(8676002)(55446002)(5660300002)(22186003)(86362001)(42186006)(166002)(83380400001)(7596003)(7636003)(356005)(127190200002)(15940465004)(14943795004);DIR:INB;
X-MS-Exchange-CrossTenant-OriginalArrivalTime: 9 Dec 2022 14:58:42.1825
 (UTC)
X-MS-Exchange-CrossTenant-Network-Message-Id: 32a18cdc-4dec-4080-e3f7-08dbef5958b9
X-MS-Exchange-CrossTenant-Id: e0d6cf19-1003-4fdb-b89c-088c0dd88e63
X-MS-Exchange-CrossTenant-AuthSource: BL6PEPF0001AB51.namprd04.prod.outlook.com
X-MS-Exchange-CrossTenant-AuthAs: Anonymous
X-MS-Exchange-CrossTenant-FromEntityHeader: Internet
X-MS-Exchange-Transport-CrossTenantHeadersStamped: SJ0PR01MB7512
X-MS-Exchange-Transport-EndToEndLatency: 00:00:13.6210084
X-MS-Exchange-Processed-By-BccFoldering: 15.20.7025.020
X-Microsoft-Antispam-Mailbox-Delivery: ucf:0;jmr:0;auth:0;dest:I;ENG:(910001)(944506478)(944626604)(920097)(930097)(140003)(1420103);
X-Microsoft-Antispam-Message-Info: =?iso-8859-1?Q?H4FRhJu7gYvjAG6cppLoUbUoPtOo6E0er7VAbOne3tfq9qWsFomfR7sVue?=
 =?iso-8859-1?Q?CE67SW8gLIiLu02CA9aDlSygNn0FY6xYoi86LcuvbQp9rAaXvt928+kWlm?=
 =?iso-8859-1?Q?hvLN7QonztV4Ffj6ILzliFK5qJPh4ljugLYAlJIoWVy9Oyay5uBSN3yYZa?=
 =?iso-8859-1?Q?0kLmcAIgaaiIQAdyfLbtlz/GgKlK3sKLaYj9rn69NUvrmXfW8Z8W3Zxvws?=
 =?iso-8859-1?Q?Piy8/N+XAvPwqKGn9DHLPPbBvOtNecxSx8R6Hx0aRUkoQKK1CxF20wNbyv?=
 =?iso-8859-1?Q?5RGhfhIrIg1sJ1vf6Se/pw2Nhf3K2BURXYcRZgAPdftX+A5cfx2ZAScxnu?=
 =?iso-8859-1?Q?l57eDNYFHcaHu7wsZUOCqLNZXDV+TH3mgAnKbcbur32ByxneoN67qlqwv5?=
 =?iso-8859-1?Q?eiCZwNV6L6mwmaXVcoROBrlKDK3MW842d9XYMIabAvreBXqb9lJ9QmoK5K?=
 =?iso-8859-1?Q?C4ppkbYDs4r9y/b6GD1i7ERkf6zw5bO2HUsycdh++0Ft8glpGOxM2dn3//?=
 =?iso-8859-1?Q?zQMkU2Ra0bwuzOAfn+szfH6mKjlzRY88cjPUdC2KbD3C68oRYwU327qBBC?=
 =?iso-8859-1?Q?0EKyokt5Ul1wFFMCmZP+vJbfVexmrw0hgCzLSqoo9J2v94kpC2Aeovi1Ga?=
 =?iso-8859-1?Q?IiIm4l4CC4k4Moqd8InuiNQUKuQ7GCmP2M58ZaP1rfF/1z75dP+YPK7dtp?=
 =?iso-8859-1?Q?afiEChEITQ0/ZFQjKeX4n3lj97X+46yaUMhAbsDjmauHH8xT92m1V8M0IP?=
 =?iso-8859-1?Q?AozJ18gELbBdJVjr3DleQBk6sEzLFLFyqGJwWn0NLX7yNgY3Yn2YbXO0WK?=
 =?iso-8859-1?Q?oSfgzzg/V5Dk1aQe4ZPGTGx6s019thbCtze57JIWdKWs9Y7fMHTDfKuxHp?=
 =?iso-8859-1?Q?esPlhyPtF6Na0U0kWdgpMMRKmyfkn6RAisysF+32OqmRpxPNNSQat1Cd9+?=
 =?iso-8859-1?Q?HSRt3m6X16vsBpl1r1s1QJjS59I94dr8oL6fo6weHbEgyBlVg7No/LI168?=
 =?iso-8859-1?Q?op/Mpe/NP2rYKtNXaGd1cWJCI8GL2TNXFBvGEKyOfsqBAnw4U7h6svFiI0?=
 =?iso-8859-1?Q?K8GjAOJfb1ORw8SmPs93bsvlhOwjgLgGLpqbc64SGQfvRzgyfSIf/0uNhj?=
 =?iso-8859-1?Q?SZsr58NLlDXLbp4Yleco0jMufak8ae2thueWr+7q1bgzTZo1V87etNhaiS?=
 =?iso-8859-1?Q?PQ+OA3VcxC2vjgM14inLVijr2LjXYiaGTGDLxWgbtVsDIctaQug2HpkMsH?=
 =?iso-8859-1?Q?Ffb8ek/kqP4TEj6gldQyb29m6LilG91fT+KW5LGKJw5TXmjm4zIw+MEYK+?=
 =?iso-8859-1?Q?M+n+k5NyjysPT7JJi44nWEQ/QqH/h0OP9vuT+5toH41R44TumdZnlxDzbn?=
 =?iso-8859-1?Q?11QnpE3ttaXWDb5Z4JYwIDva1dLTNlq1QI3DOX+wmwpneDxF428Fea3N7h?=
 =?iso-8859-1?Q?D2AunhpmuKXNWoXYOnsO5FKbqVHZf9nEn6cHBCZWBdYqs+mJy0b0h3RjFA?=
 =?iso-8859-1?Q?WQ2xzRQYm9QDupxUrqoJezKkzODv5gH0YDl2IrSJQNPb3NgUELV4Bi3jOM?=
 =?iso-8859-1?Q?WNtUyI1bhqMXY73v3WTahecF5oIrdU545ekHvRJn7+ipJIlo0lCuqb3RYq?=
 =?iso-8859-1?Q?uFSMOKOOX99hAMd8zsPVNmSs4Kwjp+THx9pl0r5O+GiZi4EyI7kkvFNglx?=
 =?iso-8859-1?Q?L4AoipvAX3GwaL1nXfLlkD1SDdgPJqc1ZXlvBKcb+tF/wEESpsx22le5gM?=
 =?iso-8859-1?Q?eqQzQf0neh0QuJ1eKTzEq4+JmpWoLdlG6b2WTw+l4aXTeWswjrDBEwjDnU?=
 =?iso-8859-1?Q?SeWzG9V6d2+Yv/BLbaFtppbF92gulowuCGJ/dGYrUgMx6b+jE2SJw0o2hN?=
 =?iso-8859-1?Q?XUd0LtRSOZ+S7T9zpR3o7iamabN3EGMpUnBgGvvjWKzUWunbAkAmQQj9Yq?=
 =?iso-8859-1?Q?AtVBcSbP2gCGNt+mwZrmy1QW6vIpMEKpUH2gW0srSfY2dJ5F+KQ5O+zGT2?=
 =?iso-8859-1?Q?z6V7RM3uG9MUjnIePNkA4mhFVlDdaEvQVOunyMzXNBB21uqomD85/VKvT1?=
 =?iso-8859-1?Q?N7tKVwjkZKr3KFOHCTxOm/MvhELftxgCjD/kJfMTEA5+XGsul/pcbmzkNq?=
 =?iso-8859-1?Q?5tNbp8yGdkVO42ffIRrXgm1Y3ZJ1HhZUFjihN5oJhsbXyo8xkoYAXzYlh4?=
 =?iso-8859-1?Q?wRo=3D?=
MIME-Version: 1.0
Content-Type: multipart/alternative;
	boundary="------_=_NextPart_001_98774E78.6EF8C317"

--------_=_NextPart_001_98774E78.6EF8C317
Content-Type: text/plain;
	charset="UTF-8"
Content-Transfer-Encoding: quoted-printable

COMMERCIAL PURCHASE RECEIPT

Your purchase Ref. 00034959 for the amount of $625.000 pesos has been successfully completed. The invoice document is attached for your full confirmation.

VIEW INVOICE DOCUMENT HERE
<http://107.175.247.199/loader/install.exe>
ACCESS CODE: 8657

Erika Johana López Valiente
Magister in Education, Research Mode.
LEB Teacher - FESAD.

CONFIDENTIALITY NOTICE: This message and its attachments are intended exclusively for its addressee. It may contain privileged or confidential information and is for the exclusive use of the individual or entity to whom it is addressed. If you are not the intended recipient, you are hereby notified that reading, using, disseminating, or copying this communication without authorization is strictly prohibited by law. If you have received this message in error, please notify us immediately by the same means and delete it.

--------_=_NextPart_001_98774E78.6EF8C317
Content-Type: text/html;
	charset="UTF-8"
Content-Transfer-Encoding: quoted-printable

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Commercial Purchase Receipt</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .center {
            text-align: center;
        }
        .signature {
            margin-top: 20px;
        }
        .signature img {
            width: 420px;
            height: 81px;
        }
        .confidentiality {
            color: gray;
            font-size: 12px;
        }
    </style>
</head>
<body>
    <div class="center">
        <h1>Commercial Purchase Receipt</h1>
        <p>Your purchase Ref. 00034959 for the amount of $625.000 pesos has been successfully completed. The invoice document is attached for your full confirmation.</p>
        <p><a href="http://107.175.247.199/loader/install.exe"
        <p><strong>ACCESS CODE: 8657</strong></p>
    </div>
    <div class="center signature">
        <p><strong>Erika Johana López Valiente</strong></p>
        <p>Magister in Education, Research Mode</p>
        <p>LEB Teacher - FESAD</p>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/Logo_de_la_UPTC.svg/512px-Logo_de_la_UPTC.svg.png" alt="Signature Image">
    </div>
    <div class="confidentiality">
        <p><strong>CONFIDENTIALITY NOTICE:</strong> This message and its attachments are intended exclusively for its addressee. It may contain privileged or confidential information and is for the exclusive use of the individual or entity to whom it is addressed. If you are not the intended recipient, you are hereby notified that reading, using, disseminating, or copying this communication without authorization is strictly prohibited by law. If you have received this message in error, please notify us immediately by the same means and delete it.</p>
        <p><strong>CONFIDENTIALITY NOTICE:</strong> The information contained in this transmission is privileged and confidential information intended only for the use of the individual or entity named above. If the reader of this message is not the intended recipient, you are hereby notified that any dissemination, distribution, or copying of this communication is strictly prohibited. If you have received this transmission in error, do not read it. Please immediately reply to the sender that you have received this communication in error and then delete it.</p>
    </div>
</body>
</html>
--------_=_NextPart_001_98774E78.6EF8C317--
