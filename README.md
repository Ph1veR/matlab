# matlab
history
%-- 02/18/2020 02:36:57 PM --%
mkdir lab2
cd lab2
diary lab2_diary
$$ simboliska matematika
%% simboliskie elementi
%% piemers
syms a11 a12 a21 a22
A = [a11 a12 ; a21 a22]
syms b11 b12 b21 b22
B = [b11 b12 ; b21 b22];
C = A*B
D = A.*B
%% Simbolisko mainigo definesana
% 1.veids
x = sym('x');
y = sym('y');
sqrt(x^2)
%% pienemsim ka x ir lielaks par 0
x = sym ('x','positive');
sqrt(x^2)
% 2.veids
syms a11 a12 a21 a22
A=[a11 a12 ; a21 a22];
A'
%% penemsim ka a11 a12 a21 a22 ir reali
syms a11 a12 a21 a22 real
A'
%% 3.veids
A = sym('a',[3 4])
%% atvasinasana
syms x
diff(x^2)
diff(sqrtx)
diff(sqrt(x))
%% parcialie atvasinajumi
syms x y
z = x^5+y^4;
diff(z,x)
diff(z,y)
%% integresana
%% nenoteiktais integralis
int(x^2,x)
sims a x
syms a x
int(x^2,a)
%% neteiktais integralis
syms x
int(x^2,x,-3,3)
double(int(x^2,x,-3,3))
%% robezas
% limit()
syms x
limit(1/(x-1),x,1,'left')
limit(1/(x-1),x,1,'righet')
limit(1/(x-1),x,1,'right')
%% vienadojuma risinasana
syms x
solve(x^2-5*x+6==0,x)
%% vienadojuma sistemas
syms x y z
atb = solve(x+y+z==21,x+y-z==1,x-y+z==9)
atb.x
atb.y
atb.z
%% izteiksmju vienkarsosana
syms x
y = (x-1)*(x-2)/((x-3)*(x-4)^2)
yd = diff(y)
simplify(yd)
%% izteiksmju vienkarsosana 2
syms x
y=(x-2)*(x-3);
y
y2 = expand(y)
%% izteiksmju vienkarsosana 3
factor(y2)
%% izteiksmju vienkarsosana 4
horner(y)
%% simboliskas konstantes
pi
format long
pi
a = vpa('pi')
b = vpa('2')
c = vpa(2)
a+b+c
digits(100)
a = vpa('pi')
sqrt(a)
digits(10)
sqrt(a)
class(a)
class(b)
%% izteiksmju "skaista " attelosana
y = (x-1)*(x-2)/((x-3)*(x-4)^2)
pretty(y)
%% izteiksmju "skaista " attelosana -2
syms x
y = sqrt(x-1)/(x-4)^5;
yltx = latex(y)
yltx2 = ['$',yltx,'$']
text(0,0.5,ylxt2,'Interpreter','latex','FontSize',32,'BackgroundColor','white')
text(0,0.5,yltx2,'Interpreter','latex','FontSize',32,'BackgroundColor','white')
text(0,0.5,yltx2,'Interpreter','latex','FontSize',32,'BackgroundColor','white');
set(gca,'Visible','off')
%% rezultatu grafiska attelosana
%% aprekinu veiksana
syms x
y =x^2;
ezplot(y)
%% aprekinu veiksana
%% rezultatu grafiska attelosana ar plot
%% (2.lab darbs 2 uzdevums)
%% 1
% pienemsim ka ir dota funkcija,kurai ir jaatrod atvasinajums,un gan funkciju,gan atvasinajumu bus jauzzime uz grafika izmantojot plot uzdotaja intervala ari ar latex bus jaizveido "legend"-a
syms x
y = x^3+2*x^2-5*x+4;
% 2
yd = diff(y)
% atrodam atvasinajumu
% 3
% 3 izteiksmes vektorizacija
% (punktinu ieliksana)
yv = vectorize(y)
ydv = vectorize(yd)
%% 4.definesim x ka skaitlu vektoru
x = -2:0.01:2;
yn = eval(yv);
ydn = eval(ydv);
%% tas bija 5 solis, izteiksmes interpretacija
% citiem vardiem, paskatas kads ir x un ielikt to
%% 6.zimesim ar plot
plot(x,yn,x,ydn)
%% 7 anotesim grafiku
yltx = latex(y);
ydltx = latex(yd)
h = legend(['$',yltx,'$'],['$',ydltxt,'$']),...
set(h,'Interpreter','Latex')
h = legend(['$',yltx,'$'],['$',ydltxt,'$']),...
set(h,'Interpreter','Latex')
h = legend(['$',yltx,'$'],['$',ydltx,'$']),...
set(h,'Interpreter','Latex')
plot(x,yn,x,ydn)
h = legend(['$',yltx,'$'],['$',ydltx,'$']),...
set(h,'Interpreter','Latex')
