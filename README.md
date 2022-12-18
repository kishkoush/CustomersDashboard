# Sample
Sample project
<!DOCTYPE html>
<html>
    <head>
        <title>Customers Dashboard</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" +
        rel="stylesheet" integrity="sha384-rbsA2VBKQhggwzxH7pPCaAqO46MgnOM80zW1RWuH61DGLwZJEdK2Kadq2F9CUG65" +
        crossorigin="anonymous">
    </head>
    <body>
        <div id="root"></div>

        <script src="Js/react.development.js"></script>
        <script src="Js/react-dom.development.js"></script>
        <script src="Js/babel.js"></script>
        <script src="Js/lodash.js"></script>
        <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>

        <script type="text/babel">
            const rootHandle =document.getElementById('root')
            const {useState}=React
            const customersData = [
  {
    "Date": "2022-12-10",
    "Phone": 9182714677,
    "Name": "A Sri Vallabha",
    "Amount": 100000
  },
  {
    "Date": "2022-12-10",
    "Phone": 9381358943,
    "Name": "Konduru Vishwesh",
    "Amount": 200000
  },
  {
    "Date": "2022-12-10",
    "Phone": 703450584,
    "Name": "D Kishore",
    "Amount": 90000
  },
  {
    "Date": "2022-12-10",
    "Phone": 8801263346,
    "Name": "B Kishan",
    "Amount": 10000
  },
  {
    "Date": "2020-04-29",
    "Phone": 9455622241,
    "Name": "Shankara Narasimhan",
    "Amount": 260
  },
  {
    "Date": "2020-04-29",
    "Phone": 9597628723,
    "Name": "Sulya Gupta",
    "Amount": 90
  },
  {
    "Date": "2020-04-29",
    "Phone": 9640338121,
    "Name": "Brahma Swamy",
    "Amount": 80
  },
  {
    "Date": "2020-04-29",
    "Phone": 9383568793,
    "Name": "Vaibhav Mulye",
    "Amount": 240
  },
  {
    "Date": "2020-04-29",
    "Phone": 9455622241,
    "Name": "Shankara Narasimhan",
    "Amount": 230
  },
  {
    "Date": "2020-04-29",
    "Phone": 9521737322,
    "Name": "Riddhi Nair",
    "Amount": 70
  },
  {
    "Date": "2020-04-29",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 80
  },
  {
    "Date": "2020-04-29",
    "Phone": 9603660688,
    "Name": "Dhenuka Dhawan",
    "Amount": 250
  },
  {
    "Date": "2020-04-29",
    "Phone": 9451926724,
    "Name": "Sahan Sibal",
    "Amount": 260
  },
  {
    "Date": "2020-04-29",
    "Phone": 9699939066,
    "Name": "Haripriya Nayak",
    "Amount": 270
  },
  {
    "Date": "2020-04-29",
    "Phone": 9590146908,
    "Name": "Sachi Loliyekar",
    "Amount": 110
  },
  {
    "Date": "2020-04-29",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 100
  },
  {
    "Date": "2020-04-29",
    "Phone": 9640338121,
    "Name": "Brahma Swamy",
    "Amount": 240
  },
  {
    "Date": "2020-04-29",
    "Phone": 9236367267,
    "Name": "Takshaka Sandal",
    "Amount": 70
  },
  {
    "Date": "2020-04-30",
    "Phone": 9969345730,
    "Name": "Kavi Edwin",
    "Amount": 210
  },
  {
    "Date": "2020-04-30",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 280
  },
  {
    "Date": "2020-04-30",
    "Phone": 9971276037,
    "Name": "Pramlocha Comar",
    "Amount": 210
  },
  {
    "Date": "2020-04-30",
    "Phone": 9241664018,
    "Name": "Utathya Ghate",
    "Amount": 260
  },
  {
    "Date": "2020-04-30",
    "Phone": 9248936762,
    "Name": "Arpana Raja",
    "Amount": 260
  },
  {
    "Date": "2020-04-30",
    "Phone": 9640338121,
    "Name": "Brahma Swamy",
    "Amount": 200
  },
  {
    "Date": "2020-04-30",
    "Phone": 9895408016,
    "Name": "Mukul Krishna",
    "Amount": 180
  },
  {
    "Date": "2020-04-30",
    "Phone": 9241664018,
    "Name": "Utathya Ghate",
    "Amount": 260
  },
  {
    "Date": "2020-04-30",
    "Phone": 9920950009,
    "Name": "Rohan Sarma",
    "Amount": 110
  },
  {
    "Date": "2020-04-30",
    "Phone": 9820224845,
    "Name": "Tanika Philip",
    "Amount": 90
  },
  {
    "Date": "2020-04-30",
    "Phone": 9383568793,
    "Name": "Vaibhav Mulye",
    "Amount": 200
  },
  {
    "Date": "2020-04-30",
    "Phone": 9732082404,
    "Name": "Kali Chaudry",
    "Amount": 290
  },
  {
    "Date": "2020-04-30",
    "Phone": 9534474777,
    "Name": "Daeva Tata",
    "Amount": 70
  },
  {
    "Date": "2020-05-01",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 160
  },
  {
    "Date": "2020-05-01",
    "Phone": 9572464275,
    "Name": "Salmalin Mehta",
    "Amount": 100
  },
  {
    "Date": "2020-05-01",
    "Phone": 9688156631,
    "Name": "Sahan Oak",
    "Amount": 200
  },
  {
    "Date": "2020-05-01",
    "Phone": 9236367267,
    "Name": "Takshaka Sandal",
    "Amount": 250
  },
  {
    "Date": "2020-05-01",
    "Phone": 9979209995,
    "Name": "Atman Mathur",
    "Amount": 140
  },
  {
    "Date": "2020-05-01",
    "Phone": 9521737322,
    "Name": "Riddhi Nair",
    "Amount": 140
  },
  {
    "Date": "2020-05-01",
    "Phone": 9265205814,
    "Name": "Daeva Peri",
    "Amount": 180
  },
  {
    "Date": "2020-05-01",
    "Phone": 9267357082,
    "Name": "Muni Wasgare",
    "Amount": 210
  },
  {
    "Date": "2020-05-01",
    "Phone": 9267357082,
    "Name": "Muni Wasgare",
    "Amount": 290
  },
  {
    "Date": "2020-05-01",
    "Phone": 9590146908,
    "Name": "Sachi Loliyekar",
    "Amount": 190
  },
  {
    "Date": "2020-05-01",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 290
  },
  {
    "Date": "2020-05-01",
    "Phone": 9241664018,
    "Name": "Utathya Ghate",
    "Amount": 180
  },
  {
    "Date": "2020-05-02",
    "Phone": 9971276037,
    "Name": "Pramlocha Comar",
    "Amount": 80
  },
  {
    "Date": "2020-05-02",
    "Phone": 9920950009,
    "Name": "Rohan Sarma",
    "Amount": 140
  },
  {
    "Date": "2020-05-02",
    "Phone": 9705384480,
    "Name": "Latif Chia",
    "Amount": 70
  },
  {
    "Date": "2020-05-02",
    "Phone": 9252350612,
    "Name": "Anushka Mody",
    "Amount": 150
  },
  {
    "Date": "2020-05-02",
    "Phone": 9688156631,
    "Name": "Sahan Oak",
    "Amount": 290
  },
  {
    "Date": "2020-05-02",
    "Phone": 9359394987,
    "Name": "Tarun Mapkar",
    "Amount": 260
  },
  {
    "Date": "2020-05-02",
    "Phone": 9747425720,
    "Name": "Markandeya Barad",
    "Amount": 100
  },
  {
    "Date": "2020-05-02",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 180
  },
  {
    "Date": "2020-05-02",
    "Phone": 9699939066,
    "Name": "Haripriya Nayak",
    "Amount": 110
  },
  {
    "Date": "2020-05-02",
    "Phone": 9590146908,
    "Name": "Sachi Loliyekar",
    "Amount": 220
  },
  {
    "Date": "2020-05-02",
    "Phone": 9820224845,
    "Name": "Tanika Philip",
    "Amount": 220
  },
  {
    "Date": "2020-05-02",
    "Phone": 9747425720,
    "Name": "Markandeya Barad",
    "Amount": 90
  },
  {
    "Date": "2020-05-03",
    "Phone": 9910042819,
    "Name": "Shanti Bajwa",
    "Amount": 100
  },
  {
    "Date": "2020-05-03",
    "Phone": 9518195948,
    "Name": "Indra Chaudry",
    "Amount": 110
  },
  {
    "Date": "2020-05-03",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 80
  },
  {
    "Date": "2020-05-03",
    "Phone": 9236367267,
    "Name": "Takshaka Sandal",
    "Amount": 100
  },
  {
    "Date": "2020-05-03",
    "Phone": 9640338121,
    "Name": "Brahma Swamy",
    "Amount": 100
  },
  {
    "Date": "2020-05-03",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 120
  },
  {
    "Date": "2020-05-03",
    "Phone": 9453085874,
    "Name": "Manu Oza",
    "Amount": 120
  },
  {
    "Date": "2020-05-03",
    "Phone": 9976945538,
    "Name": "Amitabha Kothari",
    "Amount": 270
  },
  {
    "Date": "2020-05-03",
    "Phone": 9910042819,
    "Name": "Shanti Bajwa",
    "Amount": 280
  },
  {
    "Date": "2020-05-03",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 200
  },
  {
    "Date": "2020-05-03",
    "Phone": 9405883814,
    "Name": "Gauri Som",
    "Amount": 220
  },
  {
    "Date": "2020-05-03",
    "Phone": 9252350612,
    "Name": "Anushka Mody",
    "Amount": 170
  },
  {
    "Date": "2020-05-04",
    "Phone": 9453085874,
    "Name": "Manu Oza",
    "Amount": 120
  },
  {
    "Date": "2020-05-04",
    "Phone": 9640338121,
    "Name": "Brahma Swamy",
    "Amount": 150
  },
  {
    "Date": "2020-05-04",
    "Phone": 9927277067,
    "Name": "Ranjan Khare",
    "Amount": 80
  },
  {
    "Date": "2020-05-04",
    "Phone": 9910042819,
    "Name": "Shanti Bajwa",
    "Amount": 250
  },
  {
    "Date": "2020-05-04",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 200
  },
  {
    "Date": "2020-05-04",
    "Phone": 9293117791,
    "Name": "Kumara Nayak",
    "Amount": 250
  },
  {
    "Date": "2020-05-04",
    "Phone": 9976945538,
    "Name": "Amitabha Kothari",
    "Amount": 110
  },
  {
    "Date": "2020-05-04",
    "Phone": 9518195948,
    "Name": "Indra Chaudry",
    "Amount": 200
  },
  {
    "Date": "2020-05-04",
    "Phone": 9518195948,
    "Name": "Indra Chaudry",
    "Amount": 130
  },
  {
    "Date": "2020-05-04",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 140
  },
  {
    "Date": "2020-05-04",
    "Phone": 9521737322,
    "Name": "Riddhi Nair",
    "Amount": 120
  },
  {
    "Date": "2020-05-04",
    "Phone": 9920950009,
    "Name": "Rohan Sarma",
    "Amount": 120
  },
  {
    "Date": "2020-05-04",
    "Phone": 9597628723,
    "Name": "Sulya Gupta",
    "Amount": 140
  },
  {
    "Date": "2020-05-04",
    "Phone": 9534474777,
    "Name": "Daeva Tata",
    "Amount": 70
  },
  {
    "Date": "2020-05-04",
    "Phone": 9009381182,
    "Name": "Mira Reddy",
    "Amount": 240
  },
  {
    "Date": "2020-05-04",
    "Phone": 9009381182,
    "Name": "Mira Reddy",
    "Amount": 160
  },
  {
    "Date": "2020-05-04",
    "Phone": 9236367267,
    "Name": "Takshaka Sandal",
    "Amount": 150
  },
  {
    "Date": "2020-05-04",
    "Phone": 9265205814,
    "Name": "Daeva Peri",
    "Amount": 180
  },
  {
    "Date": "2020-05-05",
    "Phone": 9451926724,
    "Name": "Sahan Sibal",
    "Amount": 170
  },
  {
    "Date": "2020-05-05",
    "Phone": 9504662177,
    "Name": "Tara Menon",
    "Amount": 230
  },
  {
    "Date": "2020-05-05",
    "Phone": 9455622241,
    "Name": "Shankara Narasimhan",
    "Amount": 200
  },
  {
    "Date": "2020-05-05",
    "Phone": 9927277067,
    "Name": "Ranjan Khare",
    "Amount": 110
  },
  {
    "Date": "2020-05-05",
    "Phone": 9521737322,
    "Name": "Riddhi Nair",
    "Amount": 90
  },
  {
    "Date": "2020-05-05",
    "Phone": 9252350612,
    "Name": "Anushka Mody",
    "Amount": 120
  },
  {
    "Date": "2020-05-05",
    "Phone": 9699939066,
    "Name": "Haripriya Nayak",
    "Amount": 70
  },
  {
    "Date": "2020-05-05",
    "Phone": 9150159527,
    "Name": "Leya Sankaran",
    "Amount": 270
  },
  {
    "Date": "2020-05-05",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 240
  },
  {
    "Date": "2020-05-05",
    "Phone": 9733555024,
    "Name": "Nirav Khalsa",
    "Amount": 110
  },
  {
    "Date": "2020-05-05",
    "Phone": 9236367267,
    "Name": "Takshaka Sandal",
    "Amount": 200
  },
  {
    "Date": "2020-05-05",
    "Phone": 9241664018,
    "Name": "Utathya Ghate",
    "Amount": 260
  },
  {
    "Date": "2020-05-06",
    "Phone": 9455622241,
    "Name": "Shankara Narasimhan",
    "Amount": 210
  },
  {
    "Date": "2020-05-06",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 250
  },
  {
    "Date": "2020-05-06",
    "Phone": 9705384480,
    "Name": "Latif Chia",
    "Amount": 160
  },
  {
    "Date": "2020-05-06",
    "Phone": 9359394987,
    "Name": "Tarun Mapkar",
    "Amount": 100
  },
  {
    "Date": "2020-05-06",
    "Phone": 9688156631,
    "Name": "Sahan Oak",
    "Amount": 210
  },
  {
    "Date": "2020-05-06",
    "Phone": 9688156631,
    "Name": "Sahan Oak",
    "Amount": 280
  },
  {
    "Date": "2020-05-06",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 110
  },
  {
    "Date": "2020-05-06",
    "Phone": 9699939066,
    "Name": "Haripriya Nayak",
    "Amount": 130
  },
  {
    "Date": "2020-05-06",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 110
  },
  {
    "Date": "2020-05-06",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 90
  },
  {
    "Date": "2020-05-06",
    "Phone": 9597628723,
    "Name": "Sulya Gupta",
    "Amount": 190
  },
  {
    "Date": "2020-05-06",
    "Phone": 9521737322,
    "Name": "Riddhi Nair",
    "Amount": 140
  },
  {
    "Date": "2020-05-06",
    "Phone": 9451926724,
    "Name": "Sahan Sibal",
    "Amount": 230
  },
  {
    "Date": "2020-05-06",
    "Phone": 9403313898,
    "Name": "Adri Dave",
    "Amount": 210
  },
  {
    "Date": "2020-05-06",
    "Phone": 9895408016,
    "Name": "Mukul Krishna",
    "Amount": 240
  },
  {
    "Date": "2020-05-06",
    "Phone": 9504662177,
    "Name": "Tara Menon",
    "Amount": 140
  },
  {
    "Date": "2020-05-07",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 140
  },
  {
    "Date": "2020-05-07",
    "Phone": 9699939066,
    "Name": "Haripriya Nayak",
    "Amount": 280
  },
  {
    "Date": "2020-05-07",
    "Phone": 9732082404,
    "Name": "Kali Chaudry",
    "Amount": 130
  },
  {
    "Date": "2020-05-07",
    "Phone": 9150159527,
    "Name": "Leya Sankaran",
    "Amount": 250
  },
  {
    "Date": "2020-05-07",
    "Phone": 9820224845,
    "Name": "Tanika Philip",
    "Amount": 290
  },
  {
    "Date": "2020-05-07",
    "Phone": 9248936762,
    "Name": "Arpana Raja",
    "Amount": 260
  },
  {
    "Date": "2020-05-07",
    "Phone": 9293117791,
    "Name": "Kumara Nayak",
    "Amount": 200
  },
  {
    "Date": "2020-05-07",
    "Phone": 9640338121,
    "Name": "Brahma Swamy",
    "Amount": 200
  },
  {
    "Date": "2020-05-07",
    "Phone": 9732082404,
    "Name": "Kali Chaudry",
    "Amount": 280
  },
  {
    "Date": "2020-05-07",
    "Phone": 9265205814,
    "Name": "Daeva Peri",
    "Amount": 70
  },
  {
    "Date": "2020-05-07",
    "Phone": 9534474777,
    "Name": "Daeva Tata",
    "Amount": 160
  },
  {
    "Date": "2020-05-07",
    "Phone": 9252350612,
    "Name": "Anushka Mody",
    "Amount": 80
  },
  {
    "Date": "2020-05-07",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 220
  },
  {
    "Date": "2020-05-07",
    "Phone": 9153022424,
    "Name": "Hastin Mangal",
    "Amount": 180
  },
  {
    "Date": "2020-05-07",
    "Phone": 9920950009,
    "Name": "Rohan Sarma",
    "Amount": 160
  },
  {
    "Date": "2020-05-07",
    "Phone": 9534474777,
    "Name": "Daeva Tata",
    "Amount": 230
  },
  {
    "Date": "2020-05-07",
    "Phone": 9359394987,
    "Name": "Tarun Mapkar",
    "Amount": 260
  },
  {
    "Date": "2020-05-07",
    "Phone": 9969345730,
    "Name": "Kavi Edwin",
    "Amount": 100
  },
  {
    "Date": "2020-05-08",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 130
  },
  {
    "Date": "2020-05-08",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 120
  },
  {
    "Date": "2020-05-08",
    "Phone": 9504662177,
    "Name": "Tara Menon",
    "Amount": 220
  },
  {
    "Date": "2020-05-08",
    "Phone": 9455622241,
    "Name": "Shankara Narasimhan",
    "Amount": 150
  },
  {
    "Date": "2020-05-08",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 90
  },
  {
    "Date": "2020-05-08",
    "Phone": 9236367267,
    "Name": "Takshaka Sandal",
    "Amount": 110
  },
  {
    "Date": "2020-05-08",
    "Phone": 9330107696,
    "Name": "Nipa Naidu",
    "Amount": 70
  },
  {
    "Date": "2020-05-08",
    "Phone": 9927277067,
    "Name": "Ranjan Khare",
    "Amount": 180
  },
  {
    "Date": "2020-05-08",
    "Phone": 9140356318,
    "Name": "Ballari Upadhyay",
    "Amount": 270
  },
  {
    "Date": "2020-05-08",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 70
  },
  {
    "Date": "2020-05-08",
    "Phone": 9518195948,
    "Name": "Indra Chaudry",
    "Amount": 180
  },
  {
    "Date": "2020-05-08",
    "Phone": 9976945538,
    "Name": "Amitabha Kothari",
    "Amount": 270
  },
  {
    "Date": "2020-05-08",
    "Phone": 9534474777,
    "Name": "Daeva Tata",
    "Amount": 210
  },
  {
    "Date": "2020-05-08",
    "Phone": 9504662177,
    "Name": "Tara Menon",
    "Amount": 210
  },
  {
    "Date": "2020-05-08",
    "Phone": 9293117791,
    "Name": "Kumara Nayak",
    "Amount": 200
  },
  {
    "Date": "2020-05-08",
    "Phone": 9293117791,
    "Name": "Kumara Nayak",
    "Amount": 140
  },
  {
    "Date": "2020-05-08",
    "Phone": 9248936762,
    "Name": "Arpana Raja",
    "Amount": 110
  },
  {
    "Date": "2020-05-08",
    "Phone": 9960294002,
    "Name": "Mitra Gounder",
    "Amount": 240
  },
  {
    "Date": "2020-05-08",
    "Phone": 9150159527,
    "Name": "Leya Sankaran",
    "Amount": 140
  },
  {
    "Date": "2020-05-08",
    "Phone": 9236367267,
    "Name": "Takshaka Sandal",
    "Amount": 250
  },
  {
    "Date": "2020-05-09",
    "Phone": 9732082404,
    "Name": "Kali Chaudry",
    "Amount": 100
  },
  {
    "Date": "2020-05-09",
    "Phone": 9521737322,
    "Name": "Riddhi Nair",
    "Amount": 140
  },
  {
    "Date": "2020-05-09",
    "Phone": 9293117791,
    "Name": "Kumara Nayak",
    "Amount": 190
  },
  {
    "Date": "2020-05-09",
    "Phone": 9590146908,
    "Name": "Sachi Loliyekar",
    "Amount": 150
  },
  {
    "Date": "2020-05-09",
    "Phone": 9688156631,
    "Name": "Sahan Oak",
    "Amount": 220
  },
  {
    "Date": "2020-05-09",
    "Phone": 9895408016,
    "Name": "Mukul Krishna",
    "Amount": 230
  },
  {
    "Date": "2020-05-09",
    "Phone": 9261697610,
    "Name": "Niloufer Handa",
    "Amount": 130
  },
  {
    "Date": "2020-05-09",
    "Phone": 9927277067,
    "Name": "Ranjan Khare",
    "Amount": 170
  },
  {
    "Date": "2020-05-09",
    "Phone": 9640338121,
    "Name": "Brahma Swamy",
    "Amount": 230
  },
  {
    "Date": "2020-05-09",
    "Phone": 9485132704,
    "Name": "Sohalia Das",
    "Amount": 250
  },
  {
    "Date": "2020-05-09",
    "Phone": 9330107696,
    "Name": "Nipa Naidu",
    "Amount": 240
  },
  {
    "Date": "2020-05-09",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 180
  },
  {
    "Date": "2020-05-09",
    "Phone": 9389644210,
    "Name": "Brahma Swamy",
    "Amount": 210
  }
]
            // Helper Functions
            const uniqueCustomers=(customers)=>{
                const result=_.uniqBy(customers,'Phone')
                return result
              }

            const orderTotal=(customers)=>{
                let sum=0 
                for(const cust of customers){
                  sum += cust.Amount
                }
                return sum
              }

            //Components
            function CustomersTable(props){
              const {customers, showDetails}=props
              return(
                <div>
                  <table className="table table-dark">
                    <thead>
                      <tr>
                        <th>Name</th>
                        <th>Phone</th>
                        <th>Show</th>
                        </tr>
                      </thead>
                      <tbody>
                        {
                          customers.map((customer)=>{
                            return(
                              <tr key={customer.Phone}>
                                <td>{customer.Name}</td>
                                <td>{customer.Phone}</td>
                                <td><button onClick={()=>{
                                  showDetails(customer)
                                }} className="btn btn-dark">Show</button></td>
                                </tr>
                            )
                          })
                        }
                          </tbody>
                    </table>
                  </div>
              )
             }
             
            function Search(props){
              const {term, handleChange}=props
              return(
                <input type='text' value={term} className="form-control" onChange={handleChange} placeholder="search"/>
              )
            }
            
            function CustomersContainer(props){
              const {customers}=props
              const [term, setTerm]=useState('')
              const onlyUniqueCustomers =uniqueCustomers(customers)
              const showDetails=(customer)=>{
                const customerOders=customers.filter(c => c.Phone === customer.Phone)

                const customerOrderTotal =orderTotal(customerOders)
                      alert(`
                              Name-${customer.Name}
                              Order Count-${customerOders.length} 
                              Order Total -${customerOrderTotal}
                              `)
              }

              const handleChange=(e)=>{
                const term=e.target.value
                setTerm(term)
              }
              const filteredUniqueCustomers =()=>{
                const result =onlyUniqueCustomers.filter((c)=>{
                  return c.Name.toLowerCase().includes(term) || c.Phone.toString().includes(term)
                })
                return result
              }
              return(

                <div className="md-3">
                    <div className='row'>
                        <div className="col-md-8">
                            <h1>Listing Customers-{onlyUniqueCustomers.length}</h1>
                        </div>
                    <div className="col-md-4">
                            <Search term={term} handleChange={handleChange}/>
                    </div>
                  </div>
                  <div className="row">
                            <div className="col-md-12">
                                  <CustomersTable customers={filteredUniqueCustomers()} showDetails={showDetails}/>
                            </div>
                      </div>
                </div>
              )
            }
            
            function StatsItem(props){
              const {count,text}=props
              
              return(
                        <div className="col-md-4">
                          <div className="card text-bg-dark mb-3">
                            <div className="card-header">
                              <h1>{count}</h1>
                              </div>
                            <div className="card-body">
                              <div className="card-title">
                                <h2>{text}</h2>
                                </div>
                            </div>
                          </div>
                          </div>
              )
            }

            function StatsContainer(props){
              const {customers}=props
              const ordersCount=customers.length
              return(
                        <div className="row">
                          <StatsItem count={ordersCount} text="Orders"/>
                          <StatsItem count={orderTotal(customers)} text="Amount"/>
                          <StatsItem count={uniqueCustomers(customers).length} text="Customers"/>
                        </div>
              )
            }
            
            function OrdersTable(props){
              const {data}=props
              return(
                <div className="col-md-6">
                <table className="table table-dark">
                  <thead>
                    <tr>
                      <th>No.of orders</th>
                      <th>Count of Customers</th>
                      </tr>
                    </thead>
                    <tbody>
                      {
                        Object.keys(data).map((ele,i)=>{
                          return(
                            <tr key={i}>
                              <td>{ ele }</td>
                              <td>{ data[ele] }</td>
                              </tr>
                          )
                        })
                      }
                      </tbody>
                  </table>
                  </div>
              )
            }
            
            function OrdersChart(props){
              const {data}=props
              google.charts.load('current', {'packages':['corechart']});
              google.charts.setOnLoadCallback(drawChart);
              
                const chartData=[
                        ['No of Orders', 'Customer Count']

                ]
                      for(const key in data){
                        chartData.push([key,data[key]])
                      } 
                function drawChart() {  

                  const data = google.visualization.arrayToDataTable(chartData)
                      

                  const options = {
                            title: 'Pie Chart'
                    };

                  const chart = new google.visualization.PieChart(document.getElementById('piechart'));

                  chart.draw(data, options);
                  }
              return(
                <div className="col-md-1">
                  <div id="piechart" style={{width:'550px', height:'350px'}}></div>
                  
                  </div>
              )
              
            }

            function OrdersContainer(props){
              const {customers}= props

              const customerFrequency=()=>{

                  const customersData = uniqueCustomers(customers)
                  const frequencyObj={1:0, 2:0, 3:0, 4:0, '5+':0}
                      customersData.forEach((customer)=>{
                          const customerOrders = customers.filter((c)=>{
                        return c.Phone === customer.Phone
                })
                        if(customerOrders.length >= 5){
                            frequencyObj['5+']++
                }else{
                          frequencyObj[customerOrders.length]++
                }
              })
              return frequencyObj
              }
                  return(
                        <div className="row">
                          <div className="col-md-12">
                            <h2>Orders Distribution</h2>
                            </div>
                          
                          <OrdersTable data={customerFrequency()}/>
                          <OrdersChart data={customerFrequency()}/>
                  </div>
              )
            }
            
            function App(props){
              const [customers, setCustomers]=useState(customersData)
              return(
                <div className="container mb-3">
                  <h1>Customers Dashboard</h1>
                  <StatsContainer customers={customers}/>
                  <CustomersContainer customers={customers}/>
                  <OrdersContainer customers={customers}/>
                  </div>
              )
            }
            
            ReactDOM.render(<App/>, rootHandle)
        </script>
    </body>
</html>
