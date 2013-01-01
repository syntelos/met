Method Signature Binding

  The class 'met.Met' provides java.lang.reflect.Method name and
  signature binding to and from java.lang.String


  Design

    Binding strategy via binary class file identity.  Source or
    description file based identity is not necessary because the
    existence of a JPL source file and its compiled target is a
    requirement with no loss of freedom for the application domain.

    The application domain is java applications performing method
    identification and binding from string identifiers for purposes
    from source and binary code generation to dynamic invocation.

    This package identifies existing methods to resolve a known fact,
    or to establish a mechanical context.


  Coding Language

    Whitespace is not accepted in any of the following code strings.

    Special characters

      .
      $
      #
      )
      (
      ,

    Package := name string using '.' hierarchical separator

    Class :=  name string using '$' inner class separator

    Method := name string

    FqType := Package '.' Class

    FqMethod :=

      FqType '#' Method '('  ')'

      FqType '#' Method '(' FqType0 ')'

      FqType '#' Method '(' FqType1 ',' FqType2 ')'


    The method code string is always terminated by a parenthetical
    group.  

    This syntax differentiates the method code string from an enum
    code string with the same code syntax but missing the terminal
    parenthetical group.  A user input string missing a terminal
    parenthetical may add the parenthetical group when the input
    context is a method reference.

    This group may be empty to identify either a method having no
    arguments or a method having only one signature in this class.

