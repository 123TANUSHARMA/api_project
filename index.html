import express from "express";
import axios from "axios";

const app = express();
const port = 3000;
const API_URL = "https://api.blockchain.com/v3/exchange";
const yourAPIKey = "f3181ed3-ec7e-488d-85be-7382a9d65118";

app.use(express.static("public"));

// Middleware to parse form data
app.use(express.urlencoded({ extended: true }));

// Middleware to set common headers
const headers = {
    'Accept': 'application/json',
    'X-API-Token': yourAPIKey
};

// Route to render the initial form
app.get("/", (req, res) => {
    res.render("index.ejs");
});
app.get("/feature", (req, res) => {
    res.render("partials/feature.ejs");
});
app.get("/about", (req, res) => {
    res.render("partials/about.ejs");
});
app.get("/faq", (req, res) => {
    res.render("partials/faq.ejs");
});
app.get("/submit", (req, res) => {
    res.render("partials/submit.ejs", {
        symbol: "",
        price: "",
        volume: "",
        lastprice: "",
    });
});
app.post("/submit", async(req, res) => {
    try {
        const ticker = req.body.ticker;

        // Fetch ticker data
        const tickerResponse = await axios.get(`${API_URL}/tickers/${ticker}`, { headers });

        // Render data on index.ejs template
        res.render("partials/submit.ejs", {
            symbol: tickerResponse.data.symbol,
            price: tickerResponse.data.price_24h,
            volume: tickerResponse.data.volume_24h,
            lastprice: tickerResponse.data.last_trade_price

        });

    } catch (error) {
        console.error(error);
        res.status(404).send(error.message);
    }
});

app.get("/order", (req, res) => {
    res.render("partials/order.ejs", {
        bpx: [],
        bqty: [],
        bnum: [],
        apx: [],
        aqty: [],
        anum: []
    });
});

app.post("/order", async(req, res) => {
    try {
        const ticker = req.body.ticker;

        // Fetch L3 order book data
        const l3Response = await axios.get(`${API_URL}/l3/${ticker}`, { headers });

        // Render data on index.ejs template
        res.render("partials/order.ejs", {
            bpx: l3Response.data.bids.map(bid => bid.px),
            bqty: l3Response.data.bids.map(bid => bid.qty),
            bnum: l3Response.data.bids.map(bid => bid.num),
            apx: l3Response.data.asks.map(ask => ask.px),
            aqty: l3Response.data.asks.map(ask => ask.qty),
            anum: l3Response.data.asks.map(ask => ask.num)
        });

    } catch (error) {
        console.error(error);
        res.status(404).send(error.message);
    }
});
app.get("/info", (req, res) => {
    res.render("partials/info.ejs", {
        base_currency: "",
        counter_currency: "",
        min_price_increment: "",
        min_order_size: "",
        max_order_size: "",
        lot_size: "",
        status: "",
        auction_price: "",
        auction_size: "",
        auction_time: "",
        imbalance: "",
    });
});

app.post("/info", async(req, res) => {
    try {
        const ticker = req.body.ticker;

        // Fetch ticker information data
        const tickerResponse = await axios.get(`${API_URL}/symbols/${ticker}`, { headers });

        // Render data on index.ejs template
        res.render("partials/info.ejs", {

            base_currency: tickerResponse.data.base_currency,
            counter_currency: tickerResponse.data.counter_currency,
            min_price_increment: tickerResponse.data.min_price_increment,
            min_order_size: tickerResponse.data.min_order_size,
            max_order_size: tickerResponse.data.max_order_size,
            lot_size: tickerResponse.data.lot_size,
            status: tickerResponse.data.status,
            auction_price: tickerResponse.data.auction_price,
            auction_size: tickerResponse.data.auction_size,
            auction_time: tickerResponse.data.auction_time,
            imbalance: tickerResponse.data.imbalance,

        });

    } catch (error) {
        console.error(error);
        res.status(404).send(error.message);
    }
});


// Start the server
app.listen(port, () => {
    console.log(`Server is running on port ${port}`);
});
