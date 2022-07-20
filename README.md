# utl-why-you-should-avoid-star-comments-in-sas
Why you should avoid star comments in sas
%let pgm=utl-why-you-should-avoid-star-comments-in-sas;

Why you should avoid star comments in sas

LESS IS MORE

FAILS

*-------------------------------------------------------------;
*                                                             ;
* Simple command macro to change mutiple blanks to one blank  ;
*                                                             ;
* %macro cuth/cmd;                                            ;
*   %do i=1 %to 20;                                           ;
*     c '  ' ' ' all;                                         ;
*   %end;                                                     ;
* %mend cuth;                                                 ;
*                                                             ;
* Fits on a function key                                      ;
*                                                             ;
*-------------------------------------------------------------;

EVEN THIS FAILS

*---------------------------------------------------------------------*;
*                                                                     *;
* Simple command macro that fits on a function key                    *;
* %macro cuth/cmd;%do i=1 %to 20;c '  ' ' ' all;%end;%mend cuth;cuth; *;
*---------------------------------------------------------------------*;

EVEN WORSE IN A MACRO

%macro tst;
 * %let x=2 ;  FAILS
 * don't ;     FAILS
 data class;
   set sashelp,class;
 run;quit;
%mend tst;
%tst;
