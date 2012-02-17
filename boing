:- use_module(library(http/thread_httpd)).
:- use_module(library(http/http_dispatch)).

:- http_handler('/', boing, []).		% (1)

server(Port) :-						% (2)
        http_server(http_dispatch, [port(Port)]).

boing(_Request) :-					% (3)
        format('Content-type: text/plain~n~n'),
        format('Boing!~n').

% Load this from swipl like so:
% [boing].
% Then from console run this:
% server(5000).