Converte HQL TO SQL 
—————————————————————————–
QueryTranslatorFactory translatorFactory = new ASTQueryTranslatorFactory();
SessionFactoryImplementor factory = (SessionFactoryImplementor) getHibernateTemplate().getSessionFactory();
QueryTranslator translator = translatorFactory.createQueryTranslator(query.toString(), query.toString(), Collections.EMPTY_MAP, factory);
translator.compile(Collections.EMPTY_MAP, false);
translator.getSQLString(); 
—————————————————————————–