### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
<soapenv:Header/>
	<soapenv:Body>
		<FlightTicketing>
			<FlightTicketingRQ Version="1.1" Language="es">
			<Login Email="user@mydomain.com" Password="pass"/>
			<Reservations>
				<Reservation>
				<ReservationLocator>N3QP5P</ReservationLocator>
				<Commission Type="Fixed" Amount="10" Currency="USD"/>
				</Reservation>
			</Reservations>
			</FlightTicketingRQ>
		</FlightTicketing>
	</soapenv:Body>
</soapenv:Envelope>
```

---
---
---

### Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <FlightTicketingResponse xmlns="http://www.juniper.es/webservice/2007/">
            <FlightTicketingRS>
                <Reservations>
                    <Reservation>
                        <Flight>
                            <Status>OK</Status>
                            <Paxes>
                                <Pax IdPax="1">
                                    <Name>A</Name>
                                    <Surname>B</Surname>
                                </Pax>
                                <Pax IdPax="2">
                                    <Name>Passenger name</Name>
                                    <Surname>Passenger surname</Surname>
                                </Pax>
                                <Pax IdPax="3">
                                    <Name>Passenger nameA</Name>
                                    <Surname>Passenger surnameA</Surname>
                                </Pax>
                                <Pax IdPax="4">
                                    <Name>Passenger nameAB</Name>
                                    <Surname>Passenger surnameAB</Surname>
                                </Pax>
                            </Paxes>
                        </Flight>
                    </Reservation>
                </Reservations>
            </FlightTicketingRS>
        </FlightTicketingResponse>
    </soap:Body>
</soap:Envelope>
```