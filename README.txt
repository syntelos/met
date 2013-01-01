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


