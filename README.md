.card{
  overflow:hidden;
}

.card-reveal .card-body {
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    bottom: 0;
    height: 100%;
    width: 100%;
    text-align: center;
}

.card-reveal .card-body .card-title {
    font-size: .75rem;
    margin: 0;
    text-transform: uppercase;
    font-weight: bolder;
    color: #4d4d4d;
}

@media (min-width: 992px) {
    .card-reveal .card-body {
        height: 100%;
        bottom: -100%;
        -webkit-transition: bottom .2s ease-in-out;
        transition: bottom .2s ease-in-out;
    }

    .card-reveal .card-img-top {
        -webkit-transition: -webkit-transform .5s ease-in-out;
        transition: -webkit-transform .5s ease-in-out;
        transition: transform .5s ease-in-out;
        transition: transform .5s ease-in-out, -webkit-transform .5s ease-in-out;
    }

    .card-reveal:hover .card-body {
        bottom: 0;
        background-color: rgba(255, 255, 255, 0.7);
    }

    .card-reveal:hover .card-img-top {
        -webkit-transform: scale(1.3);
        transform: scale(1.3);
    }
}

@media (min-width: 576px) and (max-width: 1199.98px) {
    .card-columns {
        -webkit-column-count: 2;
        -moz-column-count: 2;
        column-count: 2;
    }
}
