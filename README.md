## ROUTES
### POST request with json body



POST http://localhost:3000/api/Bisection-Method/ 
```JSON
{
    "eq":"e^(-x/4)*(2-x)-1",
    "xl":"0",
    "xr":"1"
}
```

POST http://localhost:3000/api/False-position-Method/
```JSON
{
	"eq":"e^(-x/4)*(2-x)-1",
	"xl":"0",
	"xr":"1"
}
```

POST http://localhost:3000/api/Newton-raphson-Method/
```JSON
{
	"eq":"sin(x)-x^2",
	"x":"1"
}
```

POST http://localhost:3000/api/One-point-iteration-Method/
```JSON
{
	"eq":"2-e^(x/4)",
	"x":"1"
}
```
POST http://localhost:3000/api/Secant-Method/
```JSON
{
	"eq":"e^x*sin(x)-1",
	"x0":"0",
	"x1":"2"
}
```
POST http://localhost:3000/api/First-Forward/
```JSON
{
	"eq":"e^(2*x)",
	"x":"2",
	"h":"0.25",
	"d":"2"
}
```
POST http://localhost:3000/api/Backward/
```JSON
{
	"eq":"e^(2*x)",
	"x":"2",
	"h":"0.25",
	"d":"2"
}
```
POST http://localhost:3000/api/Central/
```JSON
{
	"eq":"e^(2*x)",
	"x":"2",
	"h":"0.25",
	"d":"2"
}
```


### Docker

```sh
docker build -t pimpisa-api .
```

```sh
docker run -dit --name pimpisa-api -p 3000:3000 -v "${pwd}:/app" pimpisa-api
```
